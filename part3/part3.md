# 3.1
### Before optimizing
frontend: 476MB

backend: 352MB

### After optimizing
frontend: 448MB [Dockerfile for frontend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.1/frontend/Dockerfile)

backend: 324MB [Dockerfile for backend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.1/backend/Dockerfile)

# 3.2
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part3/3.2/Dockerfile)
```
docker build -t yle-dl .
docker run -v $(pwd):/app yle-dl https://areena.yle.fi/1-50151655
```
# 3.3
[Dockerfile for frontend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.3/frontend/Dockerfile)

[Dockerfile for backend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.3/backend/Dockerfile)

# 3.4
### Before using node:alpine
frontend: 448MB

backend: 352MB

### After using node:alpine
frontend: 235MB [Dockerfile for frontend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.4/frontend/Dockerfile)


backend: 139MB [Dockerfile for frontend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.4/backend/Dockerfile)

# 3.5
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part3/3.5/Dockerfile/)

# 3.6
[Dockerfile before optimizing](https://github.com/yumoL/docker_exercises/blob/master/part1/1.13/Dockerfile)

[Dockerfile after optimizing](https://github.com/yumoL/docker_exercises/blob/master/part3/3.6/Dockerfile)

