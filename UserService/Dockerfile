FROM openjdk:21

# Set all environment variables during build
ENV SPRING_DATASOURCE_URL=jdbc:mysql://host.docker.internal:3306/userservice
ENV SPRING_DATASOURCE_USERNAME=user99
ENV SPRING_JPA_HIBERNATE_DDL_AUTO=update
ENV SERVER_PORT=8200
ENV EUREKA=http://host.docker.internal:8100/eureka
ENV REDIS_HOST: host.docker.internal
ENV REDIS_PORT: 6379

ENV EUREKA_INSTANCE_HOSTNAME host.docker.internal


# Copy the jar file
COPY target/userservicetestfinal-0.0.1-SNAPSHOT.jar userservice.jar

# Expose the port
EXPOSE 8200

# Run the application
ENTRYPOINT ["java","-jar","userservice.jar"]