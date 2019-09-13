FROM openjdk AS builder

WORKDIR /app

COPY . .
RUN ./mvnw package

FROM openjdk

WORKDIR /app

COPY --from=builder /app/target/docker-example-1.1.3.jar target/docker-example-1.1.3.jar

RUN useradd -m javauser && \
    chown -R javauser /app

CMD java -jar ./target/docker-example-1.1.3.jar
