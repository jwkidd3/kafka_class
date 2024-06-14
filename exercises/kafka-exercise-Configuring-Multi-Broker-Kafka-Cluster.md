# Exercise: Configuring Multi-Broker Kafka Cluster

In this exercise you will configure a Kafka cluster with 3 brokers.

Duration: **30 mins**

## Procedure

1. Review **config/zookeeper.properties** default configuration file of Zookeeper
1. Start a Zookeeper server
    * Use **zookeeper-server-start.sh** shell script
1. Use jps -lm to make sure no brokers are running
1. Make 3 copies of server.properties
   * Make changes to the three configs to enable a multibroker cluster: id, log, port 
1. Start a Kafka broker with the first configuration
    * use server.1.properties
    * Use **kafka-server-start.sh** shell script
1. Use jps -lm to make sure that 1 broker is running
1. Start another Kafka broker with the 2nd server.properties file
    * Create a separate **server.properties** configuration file, e.g. **server.2.properties**
    * Set other configuration properties to have the server up and running
1. Use jps -lm to make sure that 2 brokers are running
1. Start another Kafka broker with the 3rd server.properties file
    * Create a separate **server.properties** configuration file, e.g. **server.3.properties**
    * Set other configuration properties to have the server up and running
1. Use jps -lm to make sure that 3 brokers are running

