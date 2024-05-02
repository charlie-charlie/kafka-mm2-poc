
## kafka-docker-mm2
Example of how to setup Kafka Docker multi cluster environment with MirrorMaker2 

## Prerequsite
Need create docker network first
```
docker network create -d bridge kafka-network-manual
```

## How to start?
```
  docker-compose -f docker-compose-kafka.yml  up
  docker-compose -f docker-compose-mm2-bi.yml up
  docker-compose -f docker-compose-mm2-uni.yml up
```

# how to start mm2?
```
docker exec -it mirror-maker /bin/bash
connect-mirror-maker /tmp/kafka/config/mm2.properties
export KAFKA_LOG4J_OPTS="-Dlog4j.configuration=file:/etc/kafka/connect-log4j.properties"
```
