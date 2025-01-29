FROM openjdk:21

# Set environment variables
ENV SERVER_PORT=8600
ENV SPRING_DATASOURCE_URL=jdbc:mysql://host.docker.internal:3306/paymentservice
ENV SPRING_DATASOURCE_USERNAME=user99
ENV SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_ISSUER_URI=http://host.docker.internal:8200
ENV EUREKA_INSTANCE_HOSTNAME=host.docker.internal
ENV EUREKA_CLIENT_SERVICE_URL_DEFAULTZONE=http://host.docker.internal:8100/eureka

# Copy the jar file
COPY target/PaymentService-0.0.1-SNAPSHOT.jar paymentservice.jar

# Expose the port
EXPOSE ${SERVER_PORT}

# Run the application
ENTRYPOINT ["java","-jar","paymentservice.jar"]