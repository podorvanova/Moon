---
layout: post
title: "Meet me halfway: Outreachy Post #4"
date: 2021-01-20
feature: 'assets/img/image4.jpg'
tag:
- Project progress
- Project timeline
- Apache Avro 
comments: true
---


## My original internship project timeline
The internship is now halfway done and this is my mid-point project progress blog post. My main goals for the first half of the internship project timeline were as follows:

1. Create initial maven module structure (including necessary directories and resource files)
2. Establish connection in my project with Elasticsearch server, read and setup required connection parameters
3. Implement parsing of the Object-to-Datastore mapping files
4. Create basic Elasticsearch types mapping and implement the necessary files for mapping representation
5. Create a required environment for the tests (implement testing with Elasticsearch container)
6. Implement simple methods for schema management (getSchemaName, createSchema, deleteSchema, schemaExists methods)
7. Implement basic input-output operations (get, put, exists methods)
8. Cover functionality which I added with tests

All of them, except for goal #7 (we will talk more about it in this post) have been achieved and successfully reviewed by my mentors.

## How it really was
It didn't always go as I wanted it to. Some project goals took longer than expected, as they required more time for research. It happened with setting up connection parameters and I had to put more time into it.

Sometimes I used to change the order of weekly tasks being as some tasks seemed more interesting and exciting to me than others. My main week #5 goals were to figure out how Elasticsearch fields are designed and appropriately implement Object-to-Datastore Mapping files. I got so caught up in it while working on my project solution that I actually did this task at the end of the third week.

I also implemented XSD validation for the XML mapping in the meantime. However, as you can see it was not in my original plan. My mentor asked me to add it, and this is a really good thing.

## This week’s tasks
Comparing my progress to the original plan, I am somewhat behind on my week #7 goals, which were not fully achieved. Week #7 goal was to implement basic input-output operations (get, put, exists methods). There were no problems with `exists` method, but `put` and `get` methods turned out to be a bit more complicated than I had originally thought.

`get` method must return a mapped Java object from Elasticsearch object corresponding to the given key. The main difficulty lies in the data deserialization. Gora uses <a href="https://avro.apache.org/docs/1.8.1/spec.html">Apache Avro</a> for data serialization & deserialization. It uses Avro schema files and transforms them into Java classes using the gora-compiler. 

Last week I tried to implement basic serialization & deserialization for primitive Avro types. I hoped to pass the simplest test for `get` method and make sure it has the right logic. However, even the simplest test case tests complex Avro type. So I have been currently working on it.

`put` method must insert the persistent Java object with the given key to Elasticsearch datastore. I did not implement completely `put` method last week as well, as data serialization is a part of the method. 

Thus, most of this week I have been working on data serialization & deserialization implementation. This is my main priority for this week.
