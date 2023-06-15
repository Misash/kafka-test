
# Kakfa-js microservice

## 1. Dependencies

   kafka v2.13-3.5.0 and node v16.13.0

## 1. Run Kafka

```bash
    #run Zookeepper
    <KAFKA_HOME>/bin/zookeeper-server-start.sh config/zookeeper.properties

    # run Kafka
    <KAFKA_HOME>/bin/kafka-server-start.sh config/server.properties
```
## 2. Create Topic

```bash
    # create topic 'test'
    <KAFKA_HOME>/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test

    # topic verification
    <KAFKA_HOME>/bin/kafka-topics.sh --list --bootstrap-server localhost:9092
```

## 3. Kafka console Producer and Consumer

```bash
    # Producer
    <KAFKA_HOME>/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

    # Consumer
    <KAFKA_HOME>/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
```

## 4. Execute Test

```bash
     npm install 
     node index.js
```




