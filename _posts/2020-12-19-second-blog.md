---
layout: post
title: "Everybody Struggles: Outreachy Post #2"
date: 2020-12-19
feature: 'assets/img/image2.jpg'
tag:
- Outreachy
- Project progress
- Project difficulties
comments: true
---


## About my project progress

Well, the third week of the internship is coming to the end, so it's time to talk about small successes and the first difficulties. Over these weeks I have been reading the documentation as never before, trying to understand the structure of the datastore schema and Elasticsearch data types, thinking over the project structure, and the main points of class interaction. Judging by my first contributions to the project, I can say that in general I manage to adhere to the project schedule, despite the difficulties that I have faced. One of them just happened this week, which pushed aside the writing of this post and took a little time to handle it.

## How to handle difficulties?

At the end of the second week, I got to the Elasticsearch data types that I need to map in the project. I discovered for myself a huge number of unknown types, some of which have no analogues in many programming languages, while others have technical difficulties with mapping.

### Communication
For example, `unsigned_long` can not be represented by the largest numeric Java type. So, the question is how to map what cannot be written in Java. After researching this topic a little, I turned to my mentor with a question. He suggested to me a very simple solution, which I knew, but for some reason did not think about it. He also told me about important mechanisms of data serialization and deserialization, which must be in my project and which I also lost from my sight.


### Research and analyze
Another type, `scaled_float`, has an additional scaling factor parameter.I have never worked before with this type, but I found an answer on how to work with this type after I looked through the code of neighbouring modules. Yes, here I was most likely lucky, but this case turned out to be indicative for me. From it I learned the following lesson: the problem has already been solved before me.

## Outcome and advice
I believe that I have laid the foundation for the project, and it will be easier further down the line. I added base types to my project, which I consider mandatory in the project. The rest will appear gradually as needed.Two advice that I would give to interns who are facing with similar difficulties:
1. Research! Frequently, the solution you are looking for most likely already exists.
2. Don't be afraid to ask mentors for advice. You may not understand something or just miss out on it, and that's okay. We all make mistakes.
