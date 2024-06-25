# MongoDB

## Server 

| Task Description         |  Command       |
|--------------------------|------------------------|
|Connect to mongodb server|`start_mongo` <br> `mongo -u root -p PASSWORD --authenticationDatabase admin local`|
|Disconnect from the server | `exit`|


## Databases

| Task Description         |  Command       |
|--------------------------|------------------------|
|Create a database |`use DATABASE_NAME`|
|List databases|`show dbs`|
|Create a collection|`db.createCollection("COLLECTION_NAME")`|
|List collections|`show collections`|
|Insert details of a record|`db.COLLECTION_NAME.insert({"FIELD_ATTRIBUTE1":"ATTRIBUTE1","FIELD_ATTRIBUTE2":"ATTRIBUTE2","FIELD_ATTRIBUTE3":"ATTRIBUTE3"})`|
|Count the number of documents inserted|`db.COLLECTION_NAME.count()`|
|List the documents|`db.COLLECTION_NAME.find()`|

<strong>What is the difference between database, collection, and document?</strong>

A database is a container for collections. Collections are analogous to tables in relational databases. A document is a record in a collection. 



## CRUD Operations

| Task Description         |  Command       |
|--------------------------|------------------------|
|Create a collection|`db.createCollection("COLLECTION_NAME")`|
|List the first document in the collection|`db.COLLECTION_NAME.findOne()`|
|List all documents in the collection|`db.COLLECTION_NAME.find()`|
|List first n documents in the collection|`db.COLLECTION_NAME.find().limit(n)`|
|Query for `ATTRIBUTE`|`db.COLLECTION_NAME.find({"FIELD_ATTRIBUTE":"ATTRIBUTE"})`|
|List all the documents with only showing `FIELD_ATTRIBUTE` in the output|`db.COLLECTION_NAME.find({},{"FIELD_ATTRIBUTE":1})`|
|List all the documents without `FIELD_ATTRIBUTE` in the output|`db.COLLECTION_NAME.find({},{"FIELD_ATTRIBUTE":0})`|
|Only show `FIELD_ATTRIBUTE2` of the documents which have `ATTRIBUTE1`|`db.COLLECTION_NAME.find({"FIELD_ATTRIBUTE1":"ATTRIBUTE1"},{"FIELD_ATTRIBUTE2":1})`|
|Add/update a field desciption|`db.COLLECTION_NAME.updateMany({DOCUMENT_TYPE},{$set:{FIELDS_TO_SET}})` <br> `{DOCUMENT_TYPE}` can be blank if you want all the documents to be updated|
|Remove documents with a cetain `ATTRIBUTE`|`db.COLLECTION_NAME.remove({"FIELD_ATTRIBUTE":"ATTRIBUTE"})` <br>|
|Remove all documents|`db.COLLECTION_NAME.remove({})`|
