Clone repo 
```bash
git clone https://github.com/Ibrahim-Adel15/Docker-1.git
```


Write your docker file
```bash 
cat <<EOF > Dockerfile
FROM amazoncorretto:17-alpine3.20

WORKDIR /app

COPY ./Docker-1/target/demo-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]
EOF
```

Build your maven application jar
```bash
mvn clean package 
```

Build docker image from Dockerfile
```bash
docker build -t app02 . 
```

Run docker container from app02 image on port 8081 
```bash
docker run -d -p 8081:8080 --name container2 app02
```

Stop container
```bash
docker stop container2
```

Delete container
```bash
docker rm container2
```