# rust-notebooks

## requirements

* [pyenv](https://github.com/pyenv/pyenv)
* [poetry](https://python-poetry.org/)
* [rustup](https://rustup.rs/)

## setup
First of all, by using `pyenv`, install a new Python interpreter which is going to be used as the **base** for yet another Python virtual environment, specifically created for this project.

```
# install the base
pyenv install 3.11.9
```

### virtual environment
Install the new Python virtual environment and all the packages specified as dependencies of this project (see `pyproject.toml`). Notice how `poetry` is going to create the new Python virtual environment in the `.venv` directory.

```
poetry install
```

### jupyter kernel
Install the EvCxR Jupyter kernel, and test if it works.

```
poetry shell
cargo install --locked evcxr_jupyter
evcxr_jupyter --install
jupyter lab
```
