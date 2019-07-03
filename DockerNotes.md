#### Run a docker image
```
docker run -d -p 8888:8888 jupyter/scipy-notebook -v /Users/lichfolky/Docker/Jupyter:/home/jovyan/work --user 501 --group-add staff
```

to get user uid and gid
```
id
```

stop / remove all of Docker containers:

```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```



docker tensorflow

docker pull tensorflow/tensorflow:latest-py3-jupyter

docker run -it --rm tensorflow/tensorflow-p 8888:8888 tensorflow/ bash

docker run -it -p 8888:8888 tensorflow/tensorflow:latest-py3-jupyter
