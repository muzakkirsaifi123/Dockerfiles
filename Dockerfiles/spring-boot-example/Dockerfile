FROM maven:3.6.0-jdk-8-alpine AS first
WORKDIR /capstone
COPY ./ ./
RUN mvn clean package
RUN echo "I am in current dir"
RUN ls -al && pwd


FROM openjdk:11-jre-slim
LABEL maintainer="Muzakkir"
COPY --from=first /capstone/target/hello-0.0.1-SNAPSHOT.jar /app/capstone.jar
ENTRYPOINT ["java","-jar","/app/capstone.jar"]