FROM openjdk:8
EXPOSE 8080

WORKDIR /srv/app
COPY ./spring-example-project/ ./spring
WORKDIR /srv/app/spring
RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
