FROM openjdk:21

# Set environment variables
ENV SERVER_PORT=8400
ENV SPRING_DATASOURCE_URL=jdbc:mysql://host.docker.internal:3306/cartservice
ENV SPRING_DATASOURCE_USERNAME=user99
ENV SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_ISSUER_URI=http://host.docker.internal:8200
ENV EUREKA_CLIENT_SERVICE_URL_DEFAULTZONE=http://host.docker.internal:8100/eureka
ENV SPRING_ELASTICSEARCH_URIS=http://host.docker.internal:9200
ENV SPRING_DATA_REDIS_HOST: host.docker.internal
ENV SPRING_DATA_REDIS_PORT: 6379

ENV EUREKA_INSTANCE_HOSTNAME host.docker.internal

# Copy the jar file
COPY target/CartService-0.0.1-SNAPSHOT.jar cartservice.jar

# Expose the port
EXPOSE ${SERVER_PORT}

# Run the application
ENTRYPOINT ["java","-jar","cartservice.jar"]