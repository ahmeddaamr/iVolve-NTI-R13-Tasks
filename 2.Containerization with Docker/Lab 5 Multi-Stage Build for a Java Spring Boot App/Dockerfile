FROM maven:3.9.14-eclipse-temurin-17-alpine

WORKDIR /app

COPY ./Docker-1 /app

RUN mvn package

FROM amazoncorretto:17-alpine3.20

WORKDIR /app

COPY --from=build /app/target/demo-0.0.1-SNAPSHOT.jar ./app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]