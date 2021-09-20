FROM openjdk:8-jdk-alpine
RUN apk add --update bash curl jq && rm -rf /var/cache/apk/*
VOLUME /tmp
ADD sellable-inventory-service-0.0.1-SNAPSHOT.jar app.jar
RUN bash -c 'touch /app.jar'
EXPOSE 9095
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]