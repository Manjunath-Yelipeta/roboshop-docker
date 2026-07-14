FROM maven:3.6.3-openjdk-17 AS builder
WORKDIR /app
COPY src ./src
COPY pom.xml .
RUN mvn clean package && \
    mv target/shipping-1.0.jar shipping.jar

FROM eclipse-temurin:17-jre-alpine
WORKDIR /app
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
COPY --from=builder --chown=roboshop:roboshop /app/shipping.jar /app/shipping.jar
USER roboshop
CMD ["java", "-jar", "shipping.jar"]

