# ANTsPyNet docker

This container is similar to the ANTsPy build, but additionally builds
ANTsPyNet.

We don't use ANTsPy as a base layer because of dependency conflicts. 


## Version and dependency information

See `requirements.txt` for the versions of ANTsPyNet and its dependencies.


## Run time data

ANTsPyNet downloads data at run time. If you run the container without Internet
access, you will need to download the data separately and then mount it within
the container at `~/.keras/ANTsXNet`.

See 

https://github.com/ANTsX/ANTsPyNet/blob/master/antspynet/utilities/get_antsxnet_data.py

for details.
