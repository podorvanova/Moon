---
layout: post
title: "Diving into the project: Outreachy Post #3"
date: 2021-01-04
feature: 'assets/img/image3.jpg'
tag:
- Apache Gora
- Project overview
- Elasticsearch
- Skills
comments: true
---


For the past month I have been working on “Add datastore for Elasticsearch” project with Apache Gora. 
This blog post will tell you more about my project and how I contribute to it. 
First, let's get to know Apache Gora.

## Apache Gora

Gora started out as an incubator at the Apache Software Foundation. 
The project has developed over time, got support and became a top-level Apache project. 
The overall goal for Apache Gora is to become the standard data representation and persistence framework for big data.

Apache Gora aims to give users easy-to-use in-memory data model and persistence for big data frameworks with data store specific mappings. 
Gora allows developers to work with data and map them into Java Objects instead of interacting directly with various datastores and their structures. 
Gora also supports analyzing the data with extensive Apache Hadoop MapReduce support, which allows making more complex operations (such as process vast amounts of data  in-parallel on large clusters of computers).

At the moment Apache Gora supports Accumulo, Aerospike, Cassandra, CouchDB, DynamoDB, HBase, Ignite, Kudu, Lucene, MongoDB, Redis, Solr datastores.
The goal of my internship is to add the same support for Elasticsearch datastore.

## Elasticsearch
Elasticsearch is a distributed full-text search engine for various data types (including textual, numerical, geospatial, structured, and unstructured), which is also used as NoSQL datastore.
Elasticsearch allows you to store, search, and analyze huge volumes of data quickly and in near real-time and give back answers in milliseconds.
The speed and scalability of Elasticsearch and its ability to index many types of content mean that it can be used for a number of use cases: search, logging and log analytics, application performance monitoring, data analysis and visualization.

Elasticsearch stores data as JSON documents.
Each document correlates a set of keys (names of fields or properties) with their corresponding values (strings, numbers, Booleans, dates, arrays of values, geolocations, or other types of data).

My tasks mainly focus on implementing a new backend (datastore) within Apache Gora, which will provide support for Elasticsearch operations, such as add, update, delete and query records.
I am also working on data type mapping between Elasticsearch and Java types.

## Skills
I think basic required skills (confident Java programming, basic NoSQL and Elasticsearch image) were enough to work on this project.
In addition to them, I also benefited greatly from knowing git and using IDE for code base navigation.
These skills helped me speed up the project, monitor the history of some similar modules inside the project and find method usages. 

I have learned much during the past months.
While working on my first tasks during the application period I understand the importance of documentation, and now I’m trying to add javadoc everywhere, where things are complex.
I believe that I have gained a new close experience with Object–relational mapping (ORM) technique that lets you query and manipulate data from a database using an object-oriented paradigm. 

The project has been giving me so much experience.
I believe that this project suits people who are interested in Java programming and working with datastores.
