# ✉️ Kafka on Docker

Kafka instance up and running with Docker on a ARM mac.

## Usage

Run at the root:

```sh
docker-compose up -d
```

### Producer

```sh

docker exec --interactive --tty broker \
kafka-console-producer --bootstrap-server localhost:9092 \
                       --topic example-topic
```

### Consumer

```sh
docker exec --interactive --tty broker \
kafka-console-consumer --bootstrap-server localhost:9092 \
                       --topic example-topic \
                       --from-beginning
```
