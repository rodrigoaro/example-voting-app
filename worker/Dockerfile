FROM maven:3.5-jdk-8-alpine AS build

WORKDIR /code

COPY . .

RUN mvn package -D skipTests


FROM openjdk:8-jre-alpine AS run

COPY --from=build /code/target/worker-jar-with-dependencies.jar worker.jar

CMD java -jar worker.jar

