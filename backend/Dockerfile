FROM openjdk:17-alpine

RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

WORKDIR /home/appuser/app

COPY target/*.jar app.jar

CMD ["java", "-jar", "app.jar"]
