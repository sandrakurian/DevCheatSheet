# MongoDB

## Server 

| Task Description         |  Command       |
|--------------------------|------------------------|
|Connect to mongodb server|`start_mongo` <br> `mongo -u root -p PASSWORD --authenticationDatabase admin local`|
|Disconnect from the server | `exit`|


## Databases

| Task Description         |  Command       |
|--------------------------|------------------------|
|Create a database |`use database_name`|
|List databases|`show dbs`|
|Create a collection|`db.createCollection("collection_name")`|
|List collections|`show collections`|
|Insert details of a record|`db.collection_name.insert({"field_attribute1":"attribute1","field_attribute2":"attribute2","field_attribute3":"attribute3"})`|
|Count the number of documents inserted|`db.collection_name.count()`|
|List the documents|`db.collection_name.find()`|

<strong>What is the difference between database, collection, and document?</strong>

A database is a container for collections. Collections are analogous to tables in relational databases. A document is a record in a collection. 



## CRUD Operations

| Task Description         |  Command       |
|--------------------------|------------------------|
|||
