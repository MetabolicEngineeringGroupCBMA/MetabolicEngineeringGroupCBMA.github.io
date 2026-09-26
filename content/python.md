---
publish: true
aliases:
  - Jupyter
  - JupyterLab
---

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
