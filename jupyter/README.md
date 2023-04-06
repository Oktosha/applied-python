# Jupyter

The notes on jupyter are in form of jupyter notebook.
Open `readme.ipynb` on Github, with VSCode or with jupyter server.

## Running jupyter server

If you have a [venv](/venv), install jupyter into it with

```bash
pip install jupyter
```

Then start the server with

```bash
jupyter notebook
```

Then open `readme.ipynb` from the jupyter interface in your browser.

## Keeping jupyter noteboooks in git

Jupyter notebooks are jsons with text, code and encoded pictures. It is perfectly fine to commit them. But I advice to add .ipynb_checkpoints to .gitignore.