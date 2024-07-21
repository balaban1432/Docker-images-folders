FROM openjdk:11-jdk-slim AS builder   
COPY . /app
WORKDIR /app
RUN javac App.java

FROM openjdk:11-jre-slim
WORKDIR /myapp
COPY --from=builder /app .
CMD ["java", "App"]
