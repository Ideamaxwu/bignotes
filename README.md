# bignotes
notes on big data study
  - [Template](#template)
  - [Flume](#flume)
  - [Kafka](#kafka)
  - [ZooKeeper](#zookeeper)
  - [Sqoop](#sqoop)
  - [Mahout](#mahout)
  - [Spark](#spark)
  - [Storm](#storm)
  - [Alluxio](#alluxio)
  - [CosmoDB](#cosmodb)
  - [Solr](#solr)
  - [biggy](#biggy)

# Template
## Intro
  - 
## Keywords
  - 
## Conc
  - 

# Flume
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
 
# Kafka
## Intro
  - Goal: distributed publish-subscribe based fault tolerant messaging system
## Keywords
  - Messaging System: Point to Point VS Publish-Subscribe
  - Topics: a stream of message, split into partitions
  - Brokers: maintain pulished data and distribute them, using ZooKeeper to keep state
  - Lead and Followers: nodes in Cluster
## Conc
  - Reliability, Scalability, Durability, Performance
  - RabbitMQ
  - More like Channel and Broker in BAD 

# ZooKeeper
## Intro
  - Goal: distributed co-ordination service to manage large set of hosts
## Keywords
  - Client and Server
  - Leader and Follower (are Server nodes)
  - znode of Persistence, Ephemeral, Sequential
## Conc
  - Reliability, Scalability, Transparency
  - Race condition, Deadlock, Inconsistency
  - Compared with Mesos, YARN (Resource Management not Coordination)
  
# Sqoop
## Intro
  - Goal: transfer data between Hadoop and relational database servers
## Keywords
  - Import and Export
  - Job
  - Codegen, Eval
## Conc
  - Alluxio, unify data at memory speed
  
# Mahout
## Intro
  - Goal: produce scalable machine learning algorithms
## Keywords
  - Recommendation, Classification, Clustering
## Conc
  - Similar tools: TensorFlow
  - Disk-based

# Spark
## Intro
  - Goal: lightning-fast in-memory cluster computing
## Keywords
  - Spark Core, SQL, Streaming, MLlib, GraphX
  - RDD against MapReduce's replication, serialization, disk IO
  - RDD Transformation
## Conc
  - Not for memory-cost computation, No file management system
  - Latency compared to Flink

# Storm
## Intro
  - Goal: distributed real-time big data-processing system
## Keywords
  - Spouts: source of stream
  - Bolts: logical processing units
  - Topology: a directed graph by connecting spouts and bolts
## Conc
  - [Post](http://nathanmarz.com/blog/history-of-apache-storm-and-lessons-learned.html)
  - Cloudera
  - Samza
  - For streaming (rather than batch)

# Alluxio
## Intro
  - 
## Keywords
  - 
## Conc
  - 

# Solr
## Intro
  - 
## Keywords
  - 
## Conc
  - 

# CosmoDB
## Intro
  - 
## Keywords
  - 
## Conc
  - 
    
# biggy
## Intro
  - Goal: Unify architecture for BDMS to provide Big Data Management Service
## Keywords
  - Unified architecture for BDMS
  - Pluggability, Automation and Intelligence
  - Five parts
## Conc
  - Berkley Data Analysis Stack
  - Reliability, Scalability, Transparency
