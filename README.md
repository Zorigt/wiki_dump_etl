# Map Music Artists in Wikipedia

#Table of Contents

* [Introduction](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#introduciton)
* [Data Set](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#data-set)
* [Data Transformations](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#data-transformations)
* [Schemas](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#schemas)
* [Live Demo](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#live-demo)
* [Presentation Deck](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#presentation-deck)
* [Instructions to Run this Pipeline](https://github.com/Zorigt/wiki_dump_etl/blob/master/README.md#instructions-to-run-this-pipeline)

#Introduciton
Map music artists who are mentioned on wiki pages of other music artists. 

#Data Set
The raw date is wiki dump XML file. It contains all wiki page articles including music artists. 

#Data Transformations
The wiki dump XML file contains tags for musicians. Therefore, the first step is to parse through the XML's page tags and stream each page tag through Kafka. Kafka then refines the page tags to select wiki pages that only include singer tags within the page tags. Kafka sends the XML page tags to HDFS and Apache Spark. HDFS store the logs and Spark further processes the singer pages into noSQL table and stores the table into Cassandra. Once the data is in Cassandra, then do the mapping of music artists with other singers who are mentioned on the wiki pages. 

#Schemas
+-------------+----------------+----------------+------+
| artist name | other artist 1 | other artist 2 | .... |
+-------------+----------------+----------------+------+
Work in progress

#Live Demo
Work in progress

#Presentation Deck
Work in progress

#Instructions to Run this Pipeline
Work in progress
