---
categories: web
---

Everyday, we search through google, click the link of a website, and contents of the website just pop up.

This seems so obvious, but how does it actually work? We'll go through details of how these web contents is delivered to us.

What we expect from a website is a view( fancy designs of a website ) which contains data(in the form of text, images, graphs... etc.) These data are present in a server. So, a client has to access server and fetch data. To achieve this, there should be a server running 24 hours a day, and it receives http request from a client, access a database with TCP protocol, fetch data(or update, delete, create) and send the result back to the client.

So, the essense of a website is to **manipulate database from client(browser), through a server**.

A website is composed of three parts. **Frontend**, **backend** and **database**.

**Frontend**
-
- Draws content on a browser
- It can't save data permanently. Instead, it draws screen based on html, css, javascript, images, and data it received from server
- html - the content that we can see on a website ( text, boxes, textareas... etc. )
- css - decorates and puts html elements on the right place. ( colors of texts, positions of boxes, background image of website... etc. )
- javascript - gives functionality to website. ( sending form data to server when a button is pressed, fetching data by requesting http request to the server... etc. )

**Backend**
-
- A computer running 24hours a day.
- Listens to requests and respond to it. (API)
- Connects to database and manipulate data
- python - django, flask, fast api...
- java - spring
- javascript - node js

**Database**
-
- Saves a huge amount of data in a efficient way
- Tree-like data structures are commonly used
- Can find data efficiently by indexing
- Schema is used to save data in a structured form
- Interacts with backend for data manipulation
- SQL - MySQL, Postgresql, Oracle DB ... etc.
- NoSQL - Mongodb, Couchdb, Dynamo DB, Firebase rdb ... etc.
- In-memory DB - redis, memcached, cassandra... etc.


> This post is for beginners and non-programmers, so strict definitions are ignored for the convinience of understanding