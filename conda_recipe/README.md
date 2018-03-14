# Conda recipe for Temporalis

Just followed [conda tutorial](https://conda.io/docs/user-guide/tutorials/build-pkgs-skeleton.html#before-you-start). 

After uploading temporalis on PyPI (just run `python setup.py sdist upload -r <server>` with server `pypitest` or `pypitest`) `cd` this folder (i.e. `conda_recipe`) , del the `bw2temporalis` folder and run

```
conda skeleton pypi bw2temporalis
```

to create `bwtemporalis/meta.yaml` file.  Add the `bld.bat` `build.sh` files in the folder to get the the conda build recipe. 


With the the conda build recipe just cd run 

```
conda-build bw2temporalis --output-folder <filepath_of_temporalis_build_file>
```

and is done. `<filepath_of_temporalis_build_file>` is the filepath of the built package. 


### Note:
 
make sure to set

```
conda config --set anaconda_upload yes
```

so every build automatically upload to anaconda several built packages


P.S: faster way to upload several 

```
In [5]: import os
   ...: for root, dirs, files in os.walk(<folder_with_all_built_packages>):
   ...:     for file in files:
   ...:         if file.endswith(".tar.bz2"):
   ...:              os.system('anaconda upload {}'.format(os.path.join(root, file)))
```
