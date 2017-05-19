# bignotes
notes on big data study
  - [Apache Flume](#apache-flume)
  - [Apache Kafka](#apache-kafka)

# Apache Flume
## Intro
  - Goal: ingests (streaming) data (e.g., logs, events) from multiple resources (e.g., web servers) into a centralized data store (e.g., HDFS, HBase)
  - Example: moves log files to Hadoop for analysis
  - HDFS put limitations: one file at a time; continuouslt generated log data
  - Workflow: data generator -> agent -> data collector -> data store
## Keywords
  - Event: Header + Byte Payload
  - Agent: from Source to Sink via Channel 
  - Channel: receives the events from the source and buffers them till they are consumed by sinks
  - Flow: multi-hop, fan-out (replicating, multiplexing)
## Conc
  - Similar tools: Facebook's Scribe, Apache Kafka
  - More like Feed in BAD
 
# Apache Kafka
## Intro
  - distributed publish-subscribe based fault tolerant messaging system
## Keywords
  - Messaging System: Point to Point VS Publish-Subscribe
  - Topics: a stream of message, split into partitions
  - Brokers: maintain pulished data and distribute them, using ZooKeeper to keep state
  - Lead and Followers: nodes in Cluster
## Conc
  - Reliability, Scalability, Durability, Performance
  - More like Channel and Broker in BAD 
