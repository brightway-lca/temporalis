# Conda recipe for Temporalis

Just followed [conda tutorial](https://conda.io/docs/user-guide/tutorials/build-pkgs-skeleton.html#before-you-start). 

After uploading temporalis on PyPI (just run `python setup.py sdist upload -r <server>` with server `pypitest` or `pypitest`) used

```
conda skeleton pypi bw2temporalis --output-dir <filepath_of_written_recipe>
```

to create yaml file which was slighlity modified (added `noarch: python` in `build`). And added `bld.bat` `build.sh` in the folder to get the the conda build recipe. 

Every new build just update the  necessary info on the `meta.yaml` i.e. `version` and `hash_value` (just get SHA256 values in the `tar.gz` from the [pypi warehouse](https://pypi.org/project/bw2temporalis/#files))

With the the conda build recipe just cd to this folder (i.e. `conda_recipe`) and run 

```
conda-build bw2temporalis --output-folder <filepath_of_temporalis_build_file>
```

and is done. `<filepath_of_temporalis_build_file>` is the filepath of the built package. 


### Note:
 
make sure to set

```
conda config --set anaconda_upload yes
```

so every build automatically upload the package
