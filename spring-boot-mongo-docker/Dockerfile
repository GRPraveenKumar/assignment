FROM maven:3.8.6-jdk-8-slim as build
WORKDIR /app
COPY . .
RUN mvn clean package

FROM openjdk:8-alpine

RUN apk update && apk add /bin/sh

RUN mkdir -p /opt/app
ENV PROJECT_HOME /opt/app

COPY --from=build /app/target/spring-boot-mongo-1.0.jar $PROJECT_HOME/spring-boot-mongo.jar

WORKDIR $PROJECT_HOME
EXPOSE 8080
CMD ["java","-jar","./spring-boot-mongo.jar"]
