# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

ARG CLIENT_PORT

# VAR_B gets the (overridden) value of VAR_A
EXPOSE $CLIENT_PORT

ENV PORT=$CLIENT_PORT

# The application's jar file
ARG JAR_FILE=target/eureka-client-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} eureka-client-0.0.1-SNAPSHOT.jar

# Run the jar file 
ENTRYPOINT ["java","-jar","eureka-client-0.0.1-SNAPSHOT.jar"]
