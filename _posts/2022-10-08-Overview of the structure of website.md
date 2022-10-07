---
categories: web
---

Everyday, we search through google, click the link of a website, and contents of the website just pops up.

This seems so obvious, but how does it actually work? We'll go through details of how these web contents is delivered to us.

What we expect from a website is to access the database from a client(browser). To achieve this, there is a server running 24 hours a day, and it receives a http request from a client, access a database with TCP protocol, fetch data(or update, delete, create) and send it back to the client.

So, we the essense of a website is to manipulate database from client.

A website is composed of three parts. **Frontend**, **backend** and **database**.

**Frontend**
-
- Draws content on browser
- It can't save data permanently. Instead, it draws screen based on html, css, javascript, images, and data it received from server
- html - the content that we can see on a website ( text, boxes, textareas... etc. )
- css - decorates and puts html elements on the right place. ( colors of text, position of boxes, background of website... etc. )
- javascript - gives functionality to website. ( sending forms to server when a button is pressed, fetching data by requesting http request to the server... etc. )

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

