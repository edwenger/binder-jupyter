# Conda environment with environment.yml

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/edwenger/binder-jupyter/master)

A Binder-compatible repo with an `environment.yml` file.

Access this Binder at the following URL:

https://mybinder.org/v2/gh/edwenger/binder-jupyter/master?filepath=index.ipynb

## Notes
The `apt.txt` installs `cmake` so we can build our custom module, which isn't available in conda.

The `environment.yml` file should list all Python libraries on which your notebooks
depend, specified as though they were created using the following `conda` commands:

```
source activate example-environment
conda env export --no-builds -f environment.yml
```

In the `postBuild` file, we clone our [custom module](https://github.com/edwenger/pybind_test), including the [`pybind11` dependency](https://github.com/pybind/pybind11) before building.
