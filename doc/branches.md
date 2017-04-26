# branches

This document explains what different branches were created for.
Branch `master` is the first one, then the newest branches are at the top.

## master

This branch always has the latest stable and global version

## storm2

Starts from storm1, but tries to implement the sceanrio in SQL, instead of code.
Still too early (17 MAR 2017). 

Per <https://storm.apache.org/releases/1.0.3/storm-sql.html>: 

> Current Limitations
>
> **Aggregation**, **windowing** and joining tables are **yet to be implemented**. Specifying parallelism hints in the topology is not yet supported. All processors have a parallelism hint of 1.
>
> Users also need to provide the dependency of the external data sources in the extlib directory. Otherwise the topology will fail to run because of ClassNotFoundException.
>
> The current implementation of the Kafka connector in StormSQL assumes both the input and the output are in JSON formats. The connector has not yet recognized the INPUTFORMAT and OUTPUTFORMAT clauses yet.

update on 26 APR: <https://storm.apache.org/releases/2.0.0-SNAPSHOT/storm-sql.html>: 

> Current Limitations
>
> Windowing is yet to be implemented.
> (...)

## storm1

Add scenario with Storm + Trident.
Not finished. 


## spark3

Add scenario with Spark Streaming - in Scala, with Spark 1.6 means instead of Spark 2, even if the engine is Spark 2.
As explained in branch Saprk 2, Spark 2 streaming is still in alpha.

## spark2

Add scenario with Spark Streaming - in Scala this time
tried to implement <http://spark.apache.org/docs/latest/structured-streaming-programming-guide.html>, but it was too early: <http://stackoverflow.com/questions/41303037/spark-2-0-2-sql-streaming-failed-to-find-data-source-kafka>.

## spark1

Add scenario with Spark Streaming - that was a tentative in Python

## flink2

Prepare demos around the Flink scenario. 


## multi1

Adds the following features to boontadata: 
- run on one node (dev) or several nodes
- leverages a docker registry
- docker-compose.yml is created depending on the scenarios that must be run
- adds a multi node support for Spark

## flink1

Adds a scenario where Apache Flink consumes data using event time.

