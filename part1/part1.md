# 1.1
### Start 3 containers
<img src=https://github.com/yumoL/docker_exercises/blob/master/shortcuts/1.1a.png>

### Stop 2 of the containers leaving 1 up
<img src=https://github.com/yumoL/docker_exercises/blob/master/shortcuts/1.1b.png>

# 1.2
<img src=https://github.com/yumoL/docker_exercises/blob/master/shortcuts/1.2.png>

# 1.3
<img src=https://github.com/yumoL/docker_exercises/blob/master/shortcuts/1.3.png>

# 1.4
<img src=https://github.com/yumoL/docker_exercises/blob/master/shortcuts/1.4.png>

# 1.5
```
docker run -d --rm -it --name reader ubuntu:16.04 sh -c 'echo "Input website:"; read website; echo "Searching";sleep 1; curl http://$website;'
```
```
docker exec -it reader bash
```
```
# inside the container
apt-get update
apt-get install curl
exit
```
```
docker attach reader
```
# 1.6
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.6/Dockerfile)
```
docker run -it docker-clock
```
# 1.7
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.7/Dockerfile)

[script](https://github.com/yumoL/docker_exercises/blob/master/part1/1.7/script.sh)
``` 
# build the image
docker build -t curler .
```
```
# run a container
docker run -it curler
```
# 1.8
```
# pull the image
docker pull devopsdockeruh/first_volume_exercise
```
```
# create a new file in host
touch logs.txt
```
```
# start the container with bind mount
docker run -v $(pwd)/logs.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise
```
# 1.9
```
docker run -p 3000:80 devopsdockeruh/ports_exercise
```
# 1.10
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.10/Dockerfile)
```
docker build -t frontend .
docker run -it -p 5000:5000 frontend
```
# 1.11
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.11/Dockerfile)
```
docker build -t backend .
touch logs.txt
docker run -it -v $(pwd)/logs.txt:/mydir/logs.txt -p 8000:8000 backend
```
# 1.12
[Dockerfile for frontend](https://github.com/yumoL/docker_exercises/tree/master/part1/1.12/frontend/Dockerfile)

[Dockerfile for backend](https://github.com/yumoL/docker_exercises/blob/master/part1/1.12/backend/Dockerfile)

```
docker build -t backend2 .
docker build -t frontend2 .
docker run -d -p 8000:8000 --name b2 backend2
docker run -d -p 5000:5000 --name f2 frontend2
```
# 1.13
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.13/Dockerfile)
```
docker build -t java_spring .
docker run -d -p 8080:8080 --name spring java_spring
```
# 1.14
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.14/Dockerfile)
```
docker build -t rails .
docker run -d -p 3000:3000 --name rail_project rails
```
# 1.15
[link to the project in Docker hub](https://hub.docker.com/r/yumol/country_information)

# 1.16
[link to Heroku](https://dashboard.heroku.com/apps/dockerexercise)

# 1.17
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part1/1.17/Dockerfile)
[link to image in Docker hub](https://hub.docker.com/r/yumol/devenv_node)
 
### Description
I created an environment where user can develope a web application using node (and react). The environment is ubuntu with node and npm downloaded. 

