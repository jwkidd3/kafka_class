# Exercise: Partition Leader Election and Consumer Fail-Over

In this exercise you will experiment with **partition leader election** and **consumer fail-over**.

Duration: **30 mins**


## Procedure

1. Create a topic **t1** with 1 partition and replication factor of 2
  * `./bin/kafka-topics.sh --create --bootstrap-server :9092 --topic t1 --partitions 1 --replication-factor 2`
  * `./bin/kafka-topics.sh --describe --bootstrap-server :9092 --topic t1`
2. Produce and consume a few messages
  * Use [kafkacat - Apache Kafka producer and consumer tool](https://github.com/edenhill/kafkacat)

At this point you should have a topic with replication factor of 2, one producer and one consumer. You made sure that communication between the clients is established (the clients can exchange messages).

3. Shut down the partition leader
4. Observe what happens with the clients and whether they can communicate with the cluster and with each other
5. Use kafka-topics to check out the leader
