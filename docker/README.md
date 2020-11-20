# ANTsPyNet docker

This container is similar to the ANTsPy build, but additionally builds
ANTsPyNet.

We don't use ANTsPy as a base layer because of dependency conflicts. 


## Version and dependency information

See `requirements.txt` for the versions of ANTsPyNet and its dependencies.

The latest ANTsPy and ANTsPyNet are installed from Github at build time. For
additional reproducibility, one can specify specific versions in the
`requirements.txt` and the `Dockerfile`. 

External dependencies have fixed versions as specified in `requirements.txt`.


## Run time data

ANTsPyNet downloads data at run time. If you run the container without Internet
access, you will need to download the data separately and then mount it within
the container. The default location for the data is `~/.keras/ANTsXNet`. This
can be changed at run time with the `antsxnet_cache_directory` option to the
relevant functions.

See 

https://github.com/ANTsX/ANTsPyNet/blob/master/antspynet/utilities/get_antsxnet_data.py

for more detail.


