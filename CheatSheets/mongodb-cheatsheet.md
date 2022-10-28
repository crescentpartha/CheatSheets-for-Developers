---
title: MongoDB CheatSheet
description: The most commonly used MongoDB commands are given here.
created: 2022-10-27
---

## Table of Contents

- [Mongo-DB CheatSheet for Developers](#mongo-db-cheatsheet-for-developers)
  - [Database Commands](#database-commands)
  - [Collection Commands](#collection-commands)
  - [Row(Document) Commands](#rowdocument-commands)
  - [MongoDB Query Operators](#mongodb-query-operators)
    - [Comparison Operators](#comparison-operators)
    - [Logical Operators](#logical-operators)
    - [Evaluation Operators](#evaluation-operators)
  - [MongoDB Update Operators](#mongodb-update-operators)
    - [Fields](#fields)
    - [Array](#array)
  - [MongoDB - Aggregation](#mongodb---aggregation)

# Mongo-DB CheatSheet for Developers

## Database Commands

|       Command       | Description                                    |
| :-----------------: | :--------------------------------------------- |
|    `createUser`     | Creates a new user.                            |
|     `show dbs`      | View all databases                             |
|    `use dbName`     | Create a new or switch databases               |
|        `db`         | View current Database                          |
| `db.dropDatabase()` | Delete Database                                |
|     `usersInfo`     | Returns information about the specified users. |

**[🔼Back to Top](#table-of-contents)**

## Collection Commands

|                 Command                  | Description                                 |
| :--------------------------------------: | :------------------------------------------ |
| `db.createCollection('collection_name')` | Create a collection named 'collection_name' |
|       `db.collection_name.drop()`        | Drop a collection named 'collection_name'   |

**[🔼Back to Top](#table-of-contents)**

## Row(Document) Commands

|                                                                                             Command                                                                                             | Description                                |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------- |
|                                                                                   `db.collection_name.find()`                                                                                   | Show all Rows in a Collection              |
|                                                                              `db.collection_name.find().pretty()`                                                                               | Show all Rows in a Collection (Prettified) |
|                                                                         `db.collection_name.findOne({name: 'ritwik'})`                                                                          | Find the first row matching the object     |
|                                                        `db.collection_name.insert({'name': 'Ritwik','lang': 'sql','member_since': 5 })`                                                         | Insert One Row                             |
| `db.collection_name.insertMany([{'name': 'Ritwik','lang': 'sql','member_since': 5}, {'name': 'Rohan','lang': 'Python','member_since': 3},{'name': 'Lovish','lang': 'Java','member_since': 4}])` | Insert many Rows                           |
|                                                                           `db.collection_name.find({lang:'Python'})`                                                                            | Search in a MongoDb Database               |
|                                                                              `db.collection_name.find().limit(2)`                                                                               | Limit the number of rows in output         |
|                                                                               `db.collection_name.find().count()`                                                                               | Count the number of rows in the output     |
|                               `db.collection_name.updateOne({name: 'Shubham'},{$set: {'name': 'Harry','lang': 'JavaScript','member_since': 51}},{upsert: true})`                                | Update a row                               |
|                                                              `db.collection_name.update({name: 'Rohan'},{$inc:{member_since: 2}})`                                                              | Mongodb Increment Operator                 |
|                                                         `db.collection_name.update({name: 'Rohan'},{$rename:{member_since: 'member'}})`                                                         | Mongodb Rename Operator                    |
|                                                                          `db.collection_name.remove({name: 'Harry'})`                                                                           | Delete Row                                 |
|                                                                         `db.collection_name.deleteOne({name: 'Harry'})`                                                                         | Delete one Row                             |
|                                                                      `db.collection_name.deleteMany({lang: 'JavaScript'})`                                                                      | Delete many Row                            |

**[🔼Back to Top](#table-of-contents)**

## MongoDB Query Operators

> There are many query operators that can be used to compare and reference document fields.

### Comparison Operators

> The following operators can be used in queries to compare values:

| Command | Description                                     |
| :-----: | :---------------------------------------------- |
|  `$eq`  | Values are equal                                |
|  `$ne`  | Values are not equal                            |
|  `$gt`  | Value is greater than another value             |
| `$gte`  | Value is greater than or equal to another value |
|  `$lt`  | Value is less than another value                |
| `$lte`  | Value is less than or equal to another value    |
|  `$in`  | Value is matched within an array                |

**[🔼Back to Top](#table-of-contents)**

### Logical Operators

> The following operators can logically compare multiple queries.

| Command | Description                                        |
| :-----: | :------------------------------------------------- |
| `$and`  | Returns documents where both queries match         |
|  `$or`  | Returns documents where either query matches       |
| `$nor`  | Returns documents where both queries fail to match |
| `$not`  | Returns documents where the query does not match   |

**[🔼Back to Top](#table-of-contents)**

### Evaluation Operators

> The following operators assist in evaluating documents.

| Command  | Description                                                        |
| :------: | :----------------------------------------------------------------- |
| `$regex` | Allows the use of regular expressions when evaluating field values |
| `$text`  | Performs a text search                                             |
| `$where` | Uses a JavaScript expression to match documents                    |

**[🔼Back to Top](#table-of-contents)**

## MongoDB Update Operators

> There are many update operators that can be used during document updates.

### Fields

> The following operators can be used to update fields:

|    Command     | Description                              |
| :------------: | :--------------------------------------- |
| `$currentDate` | Sets the field value to the current date |
|     `$inc`     | Increments the field value               |
|   `$rename`    | Renames the field                        |
|     `$set`     | Sets the value of a field                |
|    `$unset`    | Removes the field from the document      |

**[🔼Back to Top](#table-of-contents)**

### Array

> The following operators assist with updating arrays.

|   Command   | Description                                             |
| :---------: | :------------------------------------------------------ |
| `$addToSet` | Adds distinct elements to an array                      |
|   `$pop`    | Removes the first or last element of an array           |
|   `$pull`   | Removes all elements from an array that match the query |
|   `$push`   | Adds an element to an array                             |

**[🔼Back to Top](#table-of-contents)**

## MongoDB - Aggregation

| Expression  | Description                                                                                                                                                       |
| :---------: | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   `$sum`    | Sums up the defined value from all documents in the collection.                                                                                                   |
|   `$avg`    | Calculates the average of all given values from all documents in the collection.                                                                                  |
|   `$min`    | Gets the minimum of the corresponding values from all documents in the collection.                                                                                |
|   `$max`    | Gets the maximum of the corresponding values from all documents in the collection.                                                                                |
|   `$push`   | Inserts the value to an array in the resulting document.                                                                                                          |
| `$addToSet` | Inserts the value to an array in the resulting document but does not create duplicates.                                                                           |
|  `$first`   | Gets the first document from the source documents according to the grouping. Typically this makes only sense together with some previously applied “$sort”-stage. |
|   `$last`   | Gets the last document from the source documents according to the grouping. Typically this makes only sense together with some previously applied “$sort”-stage.  |

**[🔼Back to Top](#table-of-contents)**
