FROM openjdk:21

# Set environment variables
ENV SERVER_PORT=8700
ENV SPRING_KAFKA_BOOTSTRAP_SERVERS=host.docker.internal:9092
ENV EUREKA_CLIENT_SERVICE_URL_DEFAULTZONE=http://host.docker.internal:8100/eureka
ENV SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_ISSUER_URI=http://host.docker.internal:8200
ENV EUREKA_INSTANCE_HOSTNAME=host.docker.internal

# Copy the jar file
COPY target/NotificationService-0.0.1-SNAPSHOT.jar notificationservice.jar

# Expose the port
EXPOSE ${SERVER_PORT}

# Run the application
ENTRYPOINT ["java","-jar","notificationservice.jar"]