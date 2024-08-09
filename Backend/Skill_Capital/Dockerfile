FROM openjdk:17
WORKDIR /app
COPY . .
RUN apt install maven
RUN ./mvn clean package
EXPOSE 8080
CMD ["java", "-jar", "target/skil_capital-0.0.1-snapshot.jar"]
