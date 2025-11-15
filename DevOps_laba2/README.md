# Лабораторная работа №2 обычная
## bad-Dockerfile
```
FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y python3
RUN apt-get install -y python3-pip  
RUN apt-get install -y vim

COPY . /app
WORKDIR /app
CMD ["python3", "app.py"]
```
## good-Dockerfile
```

FROM python:3.9-slim

WORKDIR /app
COPY app.py .
CMD ["python", "app.py"]

```
## app.py
```print("Hello, DevOps_laba2")```