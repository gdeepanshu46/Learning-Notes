# MongoDB.

- It is a NoSQL database
- It is called as document database, as data or record are stored as documents
- It uses JSON(JavaScript Object Notation) structure to store data more specifically BSON (Binary JSON)
- Collections are very similar to tables in relational dbs, they hold records or documents
- Rows are documents while columns are fields

## Advantages over relational dbs

- Ease of development

- They are really easy to scale as compared to SQL 

## Commands in MongoDB

- ``` show dbs - show available dbs
  show dbs - show available dbs
  ```

- ```
  use myfirstdb - creates and switches to new db
  ```

- ```
  db.createUser({ user : "tiku", pwd : "9180", roles : ["readWrite", "dbAdmin"]}) 
  - creating a db user
  ```

- ```
  db.createCollection('customers') - creating a collection
  ```

- ```
  show collections
  ```

- ```
  db.customers.insert({first_name : 'tiku', last_name : 'gupta'}) 
  - creating a document in a collection
  ```

- ```
  db.customers.find() - gives a list of all documents in collection customer
  ```

- ```
  db.customers.find().pretty() - a pretty way to view documents
  ```

- ```
  db.customers.insert( [ {first_name : 'tiku', last_name : 'gupta'}, {first_name : 'amit', last_name : 'gupta', gender : 'male'} ] )  
  - inserting a list of documents in the collection
  ```

- ```
  db.customers.update( {first_name : 'tiku'}, {first_name : 'tiku', last_name : 'gupta', gender : 'male'} ) 
  - updates all record with first_name as 'tiku' to first_name : 'tiku', last_name : 'gupta' and gender : 'male'
  ```

- ```
  db.customers.update( {first_name : 'tiku'}, {$set : {gender : 'male'}} ) 
  - it will keep all the other values and set gender to 'male'
  ```

- ```
  db.customers.update({first_name : 'tiku'} , {$inc : {age : 1}}) - increment age by 1
  ```

- ```
  db.customers.update({first_name : 'tiku'} , {$unset : {age : 1}}) 
  - removing some property from the document
  ```

- ```
  db.customers.update({first_name : 'mary'} , {first_name : 'mary', last_name : 'shinde', age : 21}, {upsert : true}) 
  - if no match found, add this update to the collection
  ```

- ```
  db.customers.update({first_name : 'tiku'} , {$rename : {'gender' : 'sex'}}) - rename property name
  ```

- ```
  db.customers.remove({first_name : 'mary'}) 
  - remove all documents with first_name as 'mary' from the collection
  ```

- ```
  db.customers.remove({first_name : 'mary'}, {justOne : true}) 
  - remove the first document with first_name as mary from the collection
  ```

- ```
  db.people.updateMany(
      { },
      { $set: { join_date: new Date() } }
  )
  - updates every document of the collection 
  ```








- 

