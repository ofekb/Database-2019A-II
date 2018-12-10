# MongoDB - set program in windows
* Download mongodb from the website:
https://www.mongodb.com/dr/fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.4-signed.msi/download

## Run Mongo server and Mongo shell

* Open the cmd
* Check your path:
```
echo %PATH%
```
* If mongodb is not in the PATH -  add it to the global path:
```
set PATH=%PATH%;C:\Program Files\MongoDB\Server\4.0\bin
```
* Add to your computer "data\db" folder with this command:
```
cd \
mkdir data\db
```
* Run a mongo server with this command:
```
mongod
```
this runs MongoDB server with : port=27017 dbpath=C:\data\db\ 
* Open a new cmd window and run:
```
mongo
```
this opens a MongoDB shell version to connecting: mongodb://127.0.0.1:27017

## Get help
* In the  MongoDB shell run:
```
db.help()
```
and get this output:
```
DB methods:
        db.adminCommand(nameOrDocument) - switches to 'admin' db, and runs command [just calls db.runCommand(...)]
        db.aggregate([pipeline], {options}) - performs a collectionless aggregation on this database; returns a cursor
        db.auth(username, password)
        db.cloneDatabase(fromhost) - deprecated
        db.commandHelp(name) returns the help for the command
        db.copyDatabase(fromdb, todb, fromhost) - deprecated
        db.createCollection(name, {size: ..., capped: ..., max: ...})
        db.createView(name, viewOn, [{$operator: {...}}, ...], {viewOptions})
        db.createUser(userDocument)
        db.currentOp() displays currently executing operations in the db
        db.dropDatabase()
        db.eval() - deprecated
        db.fsyncLock() flush data to disk and lock server for backups
        db.fsyncUnlock() unlocks server following a db.fsyncLock()
        db.getCollection(cname) same as db['cname'] or db.cname
        db.getCollectionInfos([filter]) - returns a list that contains the names and options of the db's collections
        db.getCollectionNames()
        db.getLastError() - just returns the err msg string
        db.getLastErrorObj() - return full status object
        db.getLogComponents()
        db.getMongo() get the server connection object
        db.getMongo().setSlaveOk() allow queries on a replication slave server
        db.getName()
        db.getPrevError()
        db.getProfilingLevel() - deprecated
        db.getProfilingStatus() - returns if profiling is on and slow threshold
        db.getReplicationInfo()
        db.getSiblingDB(name) get the db at the same server as this one
        db.getWriteConcern() - returns the write concern used for any operations on this db, inherited from server object if set
        db.hostInfo() get details about the server's host
        db.isMaster() check replica primary status
        db.killOp(opid) kills the current operation in the db
        db.listCommands() lists all the db commands
        db.loadServerScripts() loads all the scripts in db.system.js
        db.logout()
        db.printCollectionStats()
        db.printReplicationInfo()
        db.printShardingStatus()
        db.printSlaveReplicationInfo()
        db.dropUser(username)
        db.repairDatabase()
        db.resetError()
        db.runCommand(cmdObj) run a database command.  if cmdObj is a string, turns it into {cmdObj: 1}
        db.serverStatus()
        db.setLogLevel(level,<component>)
        db.setProfilingLevel(level,slowms) 0=off 1=slow 2=all
        db.setWriteConcern(<write concern doc>) - sets the write concern for writes to the db
        db.unsetWriteConcern(<write concern doc>) - unsets the write concern for writes to the db
        db.setVerboseShell(flag) display extra information in shell output
        db.shutdownServer()
        db.stats()
        db.version() current version of the server
```

## Create or drop DB
* Create a new DB named "books":
```
use books
```
this outputs:
```
switched to db books
```
*NOTE*: `use` will switch to the given DB:
    * If the DB does not exist - a new DB will be created
    * If the DB exist - the existing DB will be used
* Print the name of the db that we use now:
```
db.getName()
```
this outputs:
```
books
```
* Get the statistics info of the current db:
```
db.stats()
```
this outputs:
```
{
        "db" : "books",
        "collections" : 0,
        "views" : 0,
        "objects" : 0,
        "avgObjSize" : 0,
        "dataSize" : 0,
        "storageSize" : 0,
        "numExtents" : 0,
        "indexes" : 0,
        "indexSize" : 0,
        "fileSize" : 0,
        "fsUsedSize" : 0,
        "fsTotalSize" : 0,
        "ok" : 1
}
```
* Drop the current Database:
```
db.dropDatabase()
```
this outputs:
```
{ "dropped" : "books", "ok" : 1 }
```

## Craete or drop collections
* Add a new collection to the current db:
```
db.createCollection("authors")
```
this outputs:
```
{ "ok" : 1 }
```
* Show all collections to the current db:
```
show collections
```
this outputs:
```
authors
```
* Drop the "authors" collection:
```
db.authors.drop()
```
this outputs:
```
true
```
* Show all collections to the current db:
```
show collections
```
we do not have any collections, so the output is empty

## CRUD for documents
***
For all the following CRUD we will use this structure:
```
use school
db.createCollection("students")
```
***

### Create documents
* `insert` - can add to the collection one or many documents. Here we add many:
```
db.students.insert([
	{
		"studentNo":"1",
		"FirstName":"Mark",
		"LastName":"Waugh",
		"Age":"10"
	},
	{
		"studentNo":"2",
		"FirstName":"Aman",
		"LastName":"Bansal",
		"Age":"25"
	},
	{
		"studentNo":"3",
		"FirstName":"Vivek",
		"LastName":"Singh",
		"Age":"30"
	}
])
```
this outputs:

```
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 3,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
```
* `insert` - can add to the collection one or many documents. Here we add one:
```
db.students.insert(
	{
		"studentNo":"4",
		"FirstName":"Dave",
		"LastName":"Sho",
		"Age":"20"
	})
```

this outputs:
```
WriteResult({ "nInserted" : 1 })
```
* `insertOne` - can add to the collection one document. Here we add one:
```
  db.students.insertOne(
	{
		"studentNo":"5",
		"FirstName":"Bob",
		"LastName":"fho",
		"Age":"20"
	})
  
```

this outputs:
```
{
        "acknowledged" : true,
        "insertedId" : ObjectId("5c0e3248b9d7b48da5d92a57")
}
```


* `insertMany` - can add to the collection many documents. Here we add many:
```
  db.students.insertMany([
	{
		"studentNo":"6",
		"FirstName":"Alice",
		"LastName":"Waugh",
		"Age":"10"
	},
	{
		"studentNo":"7",
		"FirstName":"Tom",
		"LastName":"Bansal",
		"Age":"25"
	}
])
```
this outputs:
```
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("5c0e3296b9d7b48da5d92a58"),
                ObjectId("5c0e3296b9d7b48da5d92a59")
        ]
}
```


### Delete documents

* Delete all documents:
``` 
db.students.remove({})
```
* Delete all documents that returns true to the condition: (here this will delete all the documents that have the value "25" in the "Age" field)
``` 
db.students.remove({"Age":"25"})
```
* Delete only the first document that returns true to the condition: (here this will delete the first document that have the value "25" in the "Age" field)
```
db.students.remove({"Age" : "25"}, 1)
```


### Update documents

* modify only the first document with specific age:
```
db.students.update(
{ "Age" :"10"},
{$set : {"LastName" : "Test",}}
)
```

* modify multiple documents with specific age
```
db.students.update(
{ "Age" :"10"},
{$set : {"LastName" : "Test",}},
{multi : true}
)
```

* save coomand is also to insert and also to update the data:
        * if the given object is not in the collection - a new document is added
        * if the given object is in the collection - a document is modified
*NOTE:* the documents are recognized by the "_id"   
For example: we do not have in the collectio a document with `"_id" : ObjectId("5b0be873f04a82a50d4d8c33")`, so we will add a new document when we run this command:
```
db.students.save(
{
      "_id" : ObjectId("5b0be873f04a82a50d4d8c33"), 
      "studentNo" : "2", 
      "FirstName" : "Aman", 
      "LastName" : "Bansal", 
      "Age" : "10" 
}
)
```
this outputs:
```
WriteResult({
        "nMatched" : 0,
        "nUpserted" : 1,
        "nModified" : 0,
        "_id" : ObjectId("5b0be873f04a82a50d4d8c33")
})
```
Now - we have a document with `"_id" : ObjectId("5b0be873f04a82a50d4d8c33")`, so we will modify the existing document when we run this command:
```
db.students.save(
{
      "_id" : ObjectId("5b0be873f04a82a50d4d8c33"), 
      "studentNo" : "2", 
      "FirstName" : "Aman", 
      "LastName" : "Bansal", 
      "Age" : "20" 
}
)
```
this outputs:
```
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
```


### Read documents
* To read all the documents in the collection:
```
db.students.find()
```