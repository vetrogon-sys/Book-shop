FROM maven:3.6-openjdk-11 AS builder

WORKDIR /build

COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .

#RUN chmod +x ./mvnw
RUN .mvnw dependency:go-offline -B -X

COPY /src ./src

RUN ./mvnw deploy

FROM openjdk:11.0-jre

WORKDIR /root/
COPY --from=0 /build/target/book-warehouse.jar book-warehouse.jar

ENTRYPOINT ["java", "-jar", "/root/book-shop.jar"]