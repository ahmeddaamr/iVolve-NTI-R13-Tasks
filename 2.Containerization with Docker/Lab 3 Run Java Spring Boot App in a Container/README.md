Clone your application repo 
```bash
git clone https://github.com/Ibrahim-Adel15/Docker-1.git
```

Write your Dockerfile
```bash
cat <<EOF > 
FROM maven:3.9.14-eclipse-temurin-17-alpine

WORKDIR /app

COPY ./Docker-1 /app

RUN mvn package

EXPOSE 8080

CMD ["java", "-jar", "target/demo-0.0.1-SNAPSHOT.jar"]
EOF
```

Build docker image from dockerfile
```bash 
docker build -t app01 . 
```

Run docker container from app01 image 
```bash
docker run -d -p 8080:8080 --name container1 app01
```

Stop container
```bash
docker stop container1
```

Delete container
```bash
docker rm container1
```