# KafkaSparkStructuredStreaming

SF Crime Statistics with Spark Streaming Project
Introduction
The aim of the project is to create an Streaming application with Spark that connects to a Kafka cluster, reads and process the data.

Requirements
Java 1.8.x
Scala 2.11.x
Spark 2.4.x
Kafka
Python 3.6 or above
How to use the application
In order to run the application you will need to start:

##Zookeeper:
`/usr/bin/zookeeper-server-start config/zookeeper.properties`

##Kafka server:
`/usr/bin/kafka-server-start config/server.properties`

##Insert data into topic:
`python3 kafka_server.py`

##Kafka consumer:
`kafka-console-consumer --topic "topic-name" --from-beginning --bootstrap-server localhost:9092`

##Run Spark job:
`spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.4.0 --master local[*] data_stream.py`

##Questions:

1- How did changing values on the SparkSession property parameters affect the throughput and latency of the data?

2- What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?

##Screenshots:
Screenshots are in the screenshots folder.
