FROM maven:3.8.4-jdk-11-slim AS builder

COPY . /src/

#WORKDIR
WORKDIR /src/

#First stage 
RUN mvn dependency:resolve
RUN mvn package

#Second stage
FROM openjdk:11-jre-slim

COPY --from=builder /src/target/worker-jar-with-dependencies.jar .

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]