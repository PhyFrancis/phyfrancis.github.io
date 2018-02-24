# Basic AWS Setup for Cloud Computing

## Absctract
In this article I am writing down how I used aws ec2 to build my own computing cluster, and run basic streaming process using Kafka, HDFS, Spark, Cassandra.

## Machines & Stacks
I used four ec2 m4.large instances, each running Ubuntu 16.04 ami. Each has 2 cores, 8G RAM, and 200G HDD disk. On this 4-node cluster, I deployed: 
* Spark cluster in stand-alone mode, with one node being master and three others being workers.
* Hadoop cluster, with the namenode being the same as the Spark master node, and other three nodes being data nodes. 
* Cassandra cluster on all four machines.
* Kafka broker and producer is running on the Spark master node, consumer is running in any Spark driver process.

The Hadoop cluster is mostly to provide its hdfs to support submitting Spark jobs in cluster mode, checkpoint for Spark’s stateful streaming process, as well as feeding Kafka producer. The data flow looks like:

![aaa](/data_flow.png)
