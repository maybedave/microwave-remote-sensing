
# UE Microwave Remote Sensing (120.030)

These are the hand-outs and exercises of the Master course Microwave Remote Sensing (120.030) at the TU Wien.

A guide for creating the notebooks and the environments in JupiterHub can be found in the file [`Index.qmd`](./Index.qmd).

# Generate Jupyter Conda environment and Jupyter Kernel from `yml`

To re-create the environment as a Jupyter kernel for execution of the notebooks, do the following:

- Open a Terminal from the same level as this Markdown README file.
- Type the following into the terminal.

```
make kernel
```

Select the kernel `mrs-env`.

# Clean-up

To remove Jupyter checkpoints run:

```
make clean
```

In order to remove the Conda environments and Jupyter kernels run:

```
make teardown
```

# Developing

Use the `environment-dev.yml` to setup a conda environment for developing the lecture notebooks. Commit notebooks without output for smaller file sizes and interactive teaching. For convenience use `nbstripout` to clean notebooks, like so:

```
pip install nbstripout
nbstripout **/*.ipynb
```

Check you code for correct syntax as we want to show off good practices. You can use flake8-nb to check your writing.

```
pip install flake8-nb
flake8-nb **/*.ipynb
```

The pre-commit hooks can be used to check whether outputs are empty. This can be achieved, like so:

```
pip install pre-commit
pre-commit install
```
