# CERL Thesaurus Networks

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/alueschow/cerl-thesaurus-networks/HEAD)

## Data used
We used a sample from the [CERL Thesaurus](https://data.cerl.org/thesaurus/) which can be found at `./data/examples/demo.csv`.

## Online tutorial
Click here to run an online Binder environment: [Start Binder environment](https://mybinder.org/v2/gh/alueschow/cerl-thesaurus-networks/HEAD).

Binder automatically builds an environment with all necessary dependencies from this repository. You can then access the Jupyter notebooks inside the `./jupyter/` folder.

More documentation can be found inside the notebooks themselves.

## Using this repository locally

### Clone the repository
`git clone https://github.com/alueschow/cerl-thesaurus-networks.git`

### Install dependencies
[Poetry](https://python-poetry.org/) is used for packaging and dependency management.
* Install [Poetry](https://python-poetry.org/)
* Run `poetry shell` inside the root folder to activate a virtual environment.
* Run `poetry install` to install all necessary dependencies.
+ **Note**: You may need to install the following packages on your machine in advance (e.g. via `apt-get`) to be able to use Bibliometa:
  - libproj-dev
  - proj-data
  - proj-bin
  - libgeos-dev

### Jupyter Notebook
Use `poetry run jupyter notebook` inside the root folder to run a local notebook server.

## Using this repository with Binder
* Export poetry's dependencies to a `requirements.txt` file by calling `poetry export --without-hashes -f requirements.txt --output requirements.txt `.
* The content of this `requirements.txt` file has to go into the `environment.yml` file in the `binder` subdirectory. In the same file, other Binder configuration such as the python version used is specified.
* The `apt.txt` file in the `binder` subdirectory contains packages that need to be available in the Binder environment (see above under __Install dependencies__).
