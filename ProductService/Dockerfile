FROM openjdk:21

# Set all environment variables during build
ENV SPRING_DATASOURCE_URL=jdbc:mysql://host.docker.internal:3306/productservice
ENV SPRING_DATASOURCE_USERNAME=user99
ENV SPRING_JPA_HIBERNATE_DDL_AUTO=none
ENV SERVER_PORT=8300
ENV EUREKA=http://host.docker.internal:8100/eureka
ENV ELASTIC_SEARCH_URI=http://host.docker.internal:9200
ENV REDIS_HOST=host.docker.internal
ENV REDIS_PORT=6379
ENV RESOURCE_SERVER=http://host.docker.internal:8200
ENV SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_JWK=http://host.docker.internal:8200/oauth2/jwks

ENV EUREKA_INSTANCE_HOSTNAME host.docker.internal

#
## Copy the jar file
COPY target/ProductService-0.0.1-SNAPSHOT.jar productservice.jar

# Expose the port
EXPOSE 8300

# Run the application
ENTRYPOINT ["java","-jar","productservice.jar"]