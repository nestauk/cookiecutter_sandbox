# Cookiecutter Sandbox Demo

## Setup

This project uses [`conda`](https://docs.conda.io/en/latest/) for virtual environment management. If you are new to `conda`, you can find the [quickstart guide here](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html).

We also utilise `direnv` via the `.envrc` file to automatically:

- Import your environment variables from `.env`
- Activate your virtual environment (_only if you comment out the relevant lines in `.envrc`_)

After installing `direnv` and `conda` on your system (we recommend doing this via [`brew`](https://brew.sh/) on macOS), you **must** run the following commands in your terminal to set up the project:

```bash
direnv allow
conda env create -f environment.yaml
conda activate cookiecutter_sandbox_demo
pip install ".[dev]"
pre-commit install --install-hooks
```

## Contributor guidelines

[Technical and working style guidelines](https://github.com/nestauk/ds-cookiecutter/blob/master/GUIDELINES.md)

---

<small><p>Project based on <a target="_blank" href="https://github.com/nestauk/ds-cookiecutter">Nesta's data science project template</a>
(<a href="http://nestauk.github.io/ds-cookiecutter">Read the docs here</a>).
</small>
