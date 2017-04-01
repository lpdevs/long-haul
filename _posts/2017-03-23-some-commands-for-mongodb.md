---
layout: post
title:  "Some commands for MongoDB"
date:   2017-03-23 20:30:00 +0700
categories: [MongoDB, NoSQL]
tags: [Commands, Database, Query database] 
---

#### MongoDB Commands
  * Create or switch to a database:
	```
	use DATABASE_NAME
	```
	
  * Check currently selected database:
    ```
	db
	```
	
  * Check database lists:
    ```
	show dbs
	```
	
  * Drop database:
    ```
	db.dropDatabase()
	```
	
  * Create collection:
    ```
	db.createCollection(name, options)
	```
	
	* name: string
	* options: Documents
	  * capped: Boolean
	  * autoIndexId: Boolean
	  * size: number
	  * max: number
	  
	* Example: 
	  * db.createCollection("myCollection");
	  * db.createCollection("mycol", { capped : true, autoIndexId : true, size : 6142800, max : 10000 } )
	
  * Show collections:
    ```
	show collections
	```
	
  * Insert document
    * Using **insert**:
    ```
	db.COLLECTION_NAME.insert(document)
	```
	
	* Using **save**:
	```
	db.COLLECTION_NAME.save(document)
	```
  
  * Query document from MongoDB collection:
    * **find**:
    ```
	db.COLLECTION_NAME.find()
	```

	* Using **pretty**:
	```
	db.COLLECTION_NAME.find().pretty()
	```
	
  * Update document:  
    ```
	db.COLLECTION_NAME.update(SELECTION_CRITERIA, UPDATED_DATA)
	```
	
  * Remove document:
    * **remove**:
    ```
	db.COLLECTION_NAME.remove(DELLETION_CRITTERIA)
	```
	
	* Or to remove one document:
	```
	db.COLLECTION_NAME.remove(DELLETION_CRITTERIA, 1)
	```
	
	* Or to remove all document:
	```
	db.COLLECTION_NAME.remove()
	```
	
  * Limit the records to display:
    ```
	db.COLLECTION_NAME.find().limit(NUMBER)
	```
	
  * Sorting documents:
    ```
	db.COLLECTION_NAME.find().sort({KEY:1})
	```
	
	  * KEY : 1  -> ascending order
	  * KEY : -1 -> descending order
	
  * Indexing:
    ```
	db.COLLECTION_NAME.ensureIndex({KEY:1})
	```
	
There are more commands. But for now, I just list some basic commands. 
I hope it is helpful. Thank you. <br />LP Devs.
