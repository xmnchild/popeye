FROM  maven:3.8.4-jdk-11-slim AS builder

WORKDIR /worker

COPY . .

RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:11-jre-slim AS run

WORKDIR /worker

COPY --from=builder /worker/target/worker-jar-with-dependencies.jar .

CMD java -jar worker-jar-with-dependencies.jar