FROM eclipse-temurin:11

RUN mkdir /app

COPY build/libs/app.jar /app

EXPOSE 8080

ENTRYPOINT ["/bin/sh", "-c", "java -Djava.security.egd=file:/dev/./urandom -jar /app/app.jar"]