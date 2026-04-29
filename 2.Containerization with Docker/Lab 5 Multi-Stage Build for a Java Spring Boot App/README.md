Clone repo 
```bash
git clone https://github.com/Ibrahim-Adel15/Docker-1.git
```

Write your docker file
```bash
cat <<EOF > Dockerfile
FROM maven:3.9.14-eclipse-temurin-17-alpine

WORKDIR /app

COPY ./Docker-1 /app

RUN mvn package

FROM amazoncorretto:17-alpine3.20

WORKDIR /app

COPY --from=build /app/target/demo-0.0.1-SNAPSHOT.jar ./app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]
EOF
```

Build docker image from dockerfile
```bash
docker build -t app03 .
```
Run docker container from app01 image 
```bash
docker run -d -p 8080:8080 --name container3 app03
```
Stop container
```bash
docker stop container3
```
Delete container
```bash
docker rm container3
```