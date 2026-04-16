Clone repo 
```
git clone https://github.com/Ibrahim-Adel15/Docker-1.git
```
build docker image from dockerfile
```
docker build -t app01 . 
```
run docker container from app01 image 
```
docker run -d -p 8080:8080 --name container1 app01
```
stop container
```
docker stop container1
```
delete container
```
docker rm container1
```