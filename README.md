# ar6-carbon-boxes
Spit out the carbon box values for the FaIR AR6 calibration

## First steps

This assumes that you are developing with `conda` and `python` 3.7, 3.8 or 3.9. These instructions should work for Windows when using Anaconda Prompt and for MacOS in Terminal (and by extension, likely will work on Linux).

1. Create environment. This will automatically create a new environment called `ar6-carbon-boxes` with the required dependencies.

```
conda env create -f environment.yml
```
2. If you want to make nice version-control friendly notebooks, which will remove all output and data upon committing, run
```
nbstripout --install
```

3. Examine .gitignore and decide where you want to put any large input or output datasets that you don't want to commit to GitHub, and fill in these paths.

## Operation

### Developing your package

Most of the time your workflow will look like this

```
conda activate ar6-carbon-boxes
jupyter notebook
```

### Updating requirements

As you build the package you might want to add more dependencies. Edit the `environment.yml` file and run
```
conda env update -f environment.yml --prune
```

Please do not overwrite the `environment.yml` file using `conda env export`, as this exports everything in your local environment including all sub-dependencies and OS-specific packages (and sometimes local paths).
