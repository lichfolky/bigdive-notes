''' Pyspark Training
# unified computing engine for parallel data processing on computer clusters
# MLlib
# Streaming
# SQL
# GraphX

unified BigData computation

don't use it as a data store, only handles computation e temporary storation
to do so: Azure Storage, Amazon S3, HDFS, Apache Cassandra and message buses as
Apache Kafka

MapReduce

Arhitecture
a cluster: group of machines, pools the resource of many machines
mani resources as they are one

cluster manager: like yarn, mesos, kubernetes or spark' cluster manager
submit spark applications to the cluster managers

spark appolications consist of a driver process and a set of executor processes

the driver process run the main() function
the executors are responsable to executing code assigned by the driver
report

there's local mode
spark written in scala but with language apis the code it's translated e runned
by JVM

scala needs to be used for some operations

Process Process -> Spark Session -> executors

spark apis,

low level unstructured APi:
RDD API resilient distributed dataset
a collection of elements partitioned

persistent RDD memorized
auto recover node failures

2 ways to access shared memory :
access hdfs file
parallelisms

ACTIONS:    laZy, are only computed when an action require to be returned by the driver program
    recomputed each time run action, but you can persist an RDD in memory


RDD ACTION CAN BE ASYNCHRONOUS

RDD PERSISTENCE in cache()

in python serialized with Pickle lib
'''
