# Project Name

## Setup

This project uses [`uv`](https://docs.astral.sh/uv/) for virtual environment management. If you are new to `uv`, you can find the [quickstart guide here](https://docs.astral.sh/uv/getting-started/).

We also utilise `direnv` via the `.envrc` file to automatically:

- Import your environment variables from `.env`
- Activate your virtual environment (_only if you comment out the relevant lines in `.envrc`_)

After installing `direnv` and `uv` on your system (we recommend doing this via [`brew`](https://brew.sh/) on macOS), you **must** run the following commands in your terminal to set up the project:

```bash
direnv allow
uv sync
uv run pre-commit install --install-hooks
```

### R Setup

_Note: even if you plan to only work in R, you still **must** set up the Python environment as described above for pre-commit hooks and other potential Python dependencies._

This project uses [`renv`](https://rstudio.github.io/renv/) for R package management. If you are new to `renv`, you can find the [quickstart guide here](https://rstudio.github.io/renv/articles/renv.html).

To set up `renv` and the R environment in this repo, run the following commands in your terminal:

```bash
Rscript -e "if (!requireNamespace('renv', quietly = TRUE)) install.packages('renv', repos='https://cloud.r-project.org')"
Rscript -e "renv::restore()"
```

As you add new R packages to your project, you can run `renv::snapshot()` to update the `renv.lock` file and commit the changes to `git`, which will ensure that others can recreate the same environment.

For working with AWS services, you will need to set up an `.Renviron` file at the root of your project specifying the region to use, for most projects this file should be:

```
AWS_DEFAULT_REGION=eu-west-2
AWS_REGION=eu-west-2
```

If you use RStudio, we recommend opening this folder via "Open Project" and committing the `.Rproj` file to your repository, as it contains useful project settings for ensuring reproducibility when others work on the project.

## Contributor guidelines

[Technical and working style guidelines](https://github.com/nestauk/ds-cookiecutter/blob/master/GUIDELINES.md)

---

<small><p>Project based on <a target="_blank" href="https://github.com/nestauk/ds-cookiecutter">Nesta's data science project template</a>
(<a href="http://nestauk.github.io/ds-cookiecutter">Read the docs here</a>).
</small>
