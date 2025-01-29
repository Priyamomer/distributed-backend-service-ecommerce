FROM openjdk:21

# Set environment variables
ENV SERVER_PORT=8100

# Copy the jar file
COPY target/DiscoveryService-0.0.1-SNAPSHOT.jar discoveryservice.jar

ENV EUREKA_INSTANCE_HOSTNAME host.docker.internal
ENV EUREKA_INSTANCE_SERVICE_URL http://host.docker.internal:8100/eureka/

# Expose the Eureka port
EXPOSE 8100

# Run the application
ENTRYPOINT ["java","-jar","discoveryservice.jar"]

