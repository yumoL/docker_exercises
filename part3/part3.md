# 3.1
### Before optimizing
frontend: 476MB

backend: 352MB

### After optimizing
frontend: 448MB

backend: 324MB

# 3.2
[Dockerfile](https://github.com/yumoL/docker_exercises/blob/master/part3/3.2/Dockerfile)
```
docker build -t yle-dl .
docker run -v $(pwd):/app yle-dl https://areena.yle.fi/1-50151655
```
# 3.3
[Dockerfile for frontend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.3/frontend/Dockerfile)

[Dockerfile for backend](https://github.com/yumoL/docker_exercises/blob/master/part3/3.3/backend/Dockerfile)

