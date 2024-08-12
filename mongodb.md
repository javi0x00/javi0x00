# :memo: Notes
## MongoDB
### Resources
- [MongoDB](https://www.mongodb.com/)
- [MongoDB Documentation](https://www.mongodb.com/docs/)
### Terms and concepts
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
- MongoDB Editions
- MongoDB Shell
- MongoDB Compass
- MongoDB Atlas
* MongoDB
  - Based on JS
  - BSON format (Binary Script Object Notation)
  * Documental (records)
    - Collections (tables)
    - 16Mb limit

- Database
- Collections
- Documents

- adding new documents
- finding documents
- sorting
- limiting data
- nested
- operators
- complex queries
- $in & $nin
- querying arrays
- deleting documents
- updating documents

- Drivers
- Connecting

- mongodb (node package)
* ODM
  - Mongoose
#### Commands
Run
```
$ mongod
$ mongo
```
Basic
```
$ mongosh
> show dbs
> use <db name>
> show collections
> db.<collection name>.insertOne({x: 1})
> db.<collection name>.insertMany([{a: 1}, {b: 2}, {c: 3}])
> db.<collection name>.find()
> db.<collection name>.find().pretty()
> db.<collection name>.find({_id: ObjectId("0x00")})
> db.<collection name>.updateOne({_id: ObjectId("0x00")}, {$set: {b: 20}})
> db.<collection name>.deleteOne({_id: ObjectId("0x00")})
> db.dropDatabase()
```
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
