# Python installation

## Pyenv

Using pyenv to manage different python versions.

Adding a new python version:

`pyenv install <python-version>`

Making a python version the system-wide default:

`pyenv global <python-version>`

Checking install python versions and which one is the global default:

`penv versions`

## Pipx

Using pipx to install standalone python applications that are used as a CLI.
Each application lives in its own venv with its dependencies.

- `pipx install <package-name>` (used default system-wide python/pip to install the package)
- `pipx install <package-name> --python=<version>`  (specify a python/pip)
  - This is mostly relevant if you need newer version of a package that is only available
  for a newer python version.

Example: poetry

## Poetry

Using poetry to manage virtual envs of applications / libraries / projects I work on.


## In Neovim

- Autoformat requires ruff to be installed in Mason
