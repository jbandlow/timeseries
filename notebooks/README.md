To start a notebook server, `cd` into the notebook directory, and run
```
$ docker run -d -p 8888:8888 -v `pwd`:/home/jovyan/work jupyter/datascience-notebook \
  start-notebook.sh --NotebookApp.token=''
```
to start a notebook with `Python 2`, `Python 3`, `R`, and `Julia` kernels available.
See the [Jupyter docker stacks repository](https://github.com/jupyter/docker-stacks/) for
more info and possibilities. Note that the `datascience-notebook` repo does not come
with `tensorflow` libraries.  Use
```
$ docker run -d -p 8888:8888 -v `pwd`:/home/jovyan/work jupyter/tensorflow-notebook \
  start-notebook.sh --NotebookApp.token=''
```
for tensorflow.

Take note of the container id that is the output of this command.  You can stop the running container with
```
$ docker stop <CONTAINER ID>
```
