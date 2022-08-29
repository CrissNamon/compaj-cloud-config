FROM openjdk:11-jdk

WORKDIR /app

COPY .mvn/ ./config-service/.mvn
COPY /config-service/src ./config-service/src
COPY /config-service/pom.xml ./config-service
COPY mvnw ./config-service
COPY pom.xml ./

WORKDIR /app/config-service

RUN ./mvnw dependency:go-offline


CMD ["./mvnw", "spring-boot:run"]