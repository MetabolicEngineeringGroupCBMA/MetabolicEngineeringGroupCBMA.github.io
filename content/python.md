---
publish: true
aliases:
  - Jupyter
  - JupyterLab
  - uv
  - spyder
---

```toml
[project]
name = "pcr-primer-screen"
version = "0.1.0"
description = "Add your description here"
authors = [
    { name = "BjornFJohansson", email = "bjornjobb@gmail.com" }
]
requires-python = ">=3.14"
dependencies = [
    "pydna[primer-screen]>=5.5.16",
]
[dependency-groups]
dev = [
    "ipykernel>=6.31.0",
    "spyder-kernels>=3.1.6",
    "pytest>=9.1.1",
    "nbval>=0.11.0",
]
[tool.uv]
package = false
```

![[python-20241018071726803.png|1302x303]]

# default config folders for ipython and jupyter

home/bjorn/.ipython/profile\_default
home/bjorn/.jupyter

# how to make a jupyter notebook from a .py script

open .py file as "Notebook" from jupyterlab
pair with notebook
save

or use jupytext

- jupytext  <https://github.com/mwouts/jupytext> (seems best!) ✅
- nbconvert <https://github.com/jupyter/nbconvert> (only notebook to other formats)
- p2j       <https://github.com/remykarem/python2jupyter> (unmaintained)
- py2nb     <https://github.com/sklam/py2nb> (unmaintained)
- notedown  <https://github.com/aaren/notedown> (unmaintained)
- ipymd     <https://github.com/rossant/ipymd> (unmaintained)

<https://gist.github.com/BjornFJohansson/5f4a62714617741007dbc13a9cd0ad14>

```
jupytext --to notebook script.py                # convert notebook.py to an .ipynb file with no outputs
jupytext --to py notebook.ipynb                 # convert notebook.ipynb to a .py file
jupytext --to notebook --execute notebook.md    # convert notebook.md to an .ipynb file and run i
jupytext --update --to notebook notebook.py     # update the input cells in the .ipynb file and preserve outputs and metadata
jupytext --set-formats ipynb,py notebook.ipynb  # Turn notebook.ipynb into a paired ipynb/py notebook
jupytext --sync notebook.ipynb                  # Update all paired representations of notebook.ipynb

jupyter labextension install @ijmbarr/jupyterlab_spellchecker # https://github.com/ijmbarr/jupyterlab_spellchecker
```

To force an update, append: ?flush\_cache=true to the viewer URL.

Jupyter uses <http://requirejs.org/> so it is possible to load javascript components into the notebook
<http://blog.thedataincubator.com/2015/08/embedding-d3-in-an-ipython-notebook>

## JupyterLab

<https://libraries.io/npm/@jupyterlab%2Fui-components>

Redux is a predictable state container for [[JavaScript]] apps <https://github.com/reduxjs/redux>

We follow the React documentation and “React & Redux in TypeScript - Static Typing Guide” for best practices on using React in TypeScript.

TeselaGen/openVectorEditor         <https://teselagen.github.io/openVectorEditor>
ElianeBriand/plasmid-sketcher
vixis/angularplasmid

## uv

Installed:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh

uv python pin 3.14

uv venv

uv init --no-package  # project layout with a top-level `main.py`, `README.md`, `.python-version`, and `pyproject.toml`

uv python list
uv python list --only-installed
uv python uninstall 3.13.12
uv python list --only-installed
uv python install 3.14
uv python install --upgrade 3.14
uv python install --upgrade 3.14


uv tool install spyder
uv tool install jupyterlab
which spyder

uv sync --all-groups
uv sync --all-groups --all-extras

```

```bash
06:00 $ locate -b '\.venv' | grep "$HOME" | grep -v '/Trash/'
/home/bjorn/Desktop/gel/.venv
/home/bjorn/Desktop/misc/sofia/05_Ficha_de_Algoritmia_Fluxogramas/.venv
/home/bjorn/Desktop/primer screen/.venv
/home/bjorn/Desktop/pydna/PYEAST/.venv
/home/bjorn/myvault/Chaetomium thermophilum/notebooks/.venv
/home/bjorn/myvault/agregação/.venv
/home/bjorn/myvault/agregação/papers/.venv
/home/bjorn/myvault/files/2026-09-25/FAS2_primer_design/.venv
/home/bjorn/myvault/files/MetabolicEngineeringGroupCBMA GitHub Org/Cunha_et_al_2017/.venv
/home/bjorn/myvault/files/file processing/pdf/join/.venv
/home/bjorn/myvault/files/file processing/sign/.venv
/home/bjorn/python_packages/PlasmidStamper/.venv
/home/bjorn/python_packages/obsidian_scripts/.venv
/home/bjorn/python_packages/pydna/.venv
/home/bjorn/python_packages/pydna-utils/.venv
/home/bjorn/python_packages/pydnaweb/.venv
/home/bjorn/python_packages/pygenome/.venv
```

---

PR: Add Auto-Detection of local .venv interpreter on project open- #26386
<https://github.com/spyder-ide/spyder/pull/26386>
