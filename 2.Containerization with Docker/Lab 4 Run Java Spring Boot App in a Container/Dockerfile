FROM amazoncorretto:17-alpine3.20

WORKDIR /app

COPY ./Docker-1/target/demo-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]