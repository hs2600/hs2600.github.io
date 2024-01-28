---
layout: post
title:  What Is MongoDB? All About the Popular Open Source Database
date:   2024-01-26 00:00:00 -0800
description:
author: horacio 
image:  '/images/mongodb.webp'
tags:   [technology]
tags_color: '#477690'
---

This tutorial introduces you to the MongoDB database. You’ll discover how to install the software, manipulate data, and apply the data design techniques to your own applications.

All examples were developed using MongoDB 5 but most will work in previous or later versions. Code can be entered directly into a client application or the MongoDB shell (mongo or mongosh) to query and update the database.

### Table of Contents

1.  [What Is MongoDB?](#what-is-mongodb)
2.  [Elements of MongoDB](#elements-of-mongodb)
3.  [How To Install MongoDB](#how-to-install-mongodb)
4.  [How To Access Your MongoDB Database](#how-to-access-your-mongodb-database)
5.  [How To Insert New Documents in MongoDB](#how-to-insert-new-documents-in-mongodb)
6.  [Simple MongoDB Queries](#simple-mongodb-queries)
7.  [Using Cursors in MongoDB](#using-cursors-in-mongodb)
8.  [How To Create Indexes in MongoDB](#how-to-create-indexes-in-mongodb)
9.  [How To Manage MongoDB Indexes](#how-to-manage-mongodb-indexes)
10.  [Using MongoDB Data Validation Schemas](#using-mongodb-data-validation-schemas)
11.  [How To Update Existing Documents in MongoDB](#how-to-update-existing-documents-in-mongodb)
12.  [How To Delete Documents in MongoDB](#how-to-delete-documents-in-mongodb)
13.  [Using Aggregation Operations in MongoDB](#using-aggregation-operations-in-mongodb)
14.  [How To Run Bulk MongoDB Operations](#how-to-run-bulk-mongodb-operations)

What Is MongoDB?[](#what-is-mongodb)
------------------------------------

MongoDB is an open source NoSQL database. NoSQL means the database does not use relational tables like a traditiona.

There is a range of NoSQL database types, but MongoDB stores data in JavaScript-like objects known as _documents_, whose content looks like this:

    {
      _id: "123",
      name: "Craig"
    }

  
Although MongoDB has become synonymous with the JavaScript-based framework Node.js, official MongoDB [database drivers](https://www.mongodb.com/docs/drivers/) are available for most frameworks, languages, and runtimes, including [Node.js](https://www.mongodb.com/docs/drivers/node/current/), PHP, and Python. You can also opt for libraries such as [Mongoose](https://www.npmjs.com/package/mongoose) that offer a higher level of abstraction or object relational mapping (ORM) features.

Unlike SQL tables, there are no structural limits on what you can store in MongoDB. Data schemas are not enforced: You can store whatever you like wherever you like. This makes MongoDB ideal for more organic — _or messy_ — data structures.

Consider a contact address book. Individuals can often have multiple telephone numbers. You could define three telephone fields in a SQL table, but that would be too many for some contacts and too few for others. Ultimately, you’ll require a separate telephone table, which adds more complexity.

In MongoDB, those telephone numbers could be defined as an unlimited array of objects in the same document:

    {
      _id: "123",
      name: "Craig",
      telephone: [
        { home: "0123456789" },
        { work: "9876543210" },
        { cell: "3141592654" }
      ]
    }

Note that MongoDB uses similar JavaScript object notation for data updates and queries, which can pose some challenges if you’re used to SQL.

Elements of MongoDB[](#elements-of-mongodb)
-------------------------------------------

Before we go any further, let’s take a look at what makes MongoDB tick. We’ll be using this vocabulary throughout this article.

*   **Document:** A single individual object in a data store, analogous to a record or row in a SQL database table.
*   **Field:** A single item of data within a document, such as a name or telephone number, analogous to a SQL field or table column.
*   **Collection:** A set of similar documents, analogous to a SQL table. While you could put all your documents into a single collection, it’s usually more practical to group them into specific types. In a contact address book you could have a collection for people and a collection for companies.
*   **Database:** A collection of related data, identical in meaning to a SQL database.
*   **Schema:** A schema defines data structures. In SQL databases you must define table definitions with associated fields and types before you can store data. This is not necessary in MongoDB although it is possible to create a schema which validates documents before they can be added to a collection.
*   **Index:** A data structure used to improve querying performance, identical in meaning to SQL indexes.
*   **Primary Key:** A unique identifier for every document. MongoDB automatically adds a unique and indexed \_id field to every document in a collection.
*   **Denormalization:** In SQL databases, “normalization” is a technique used to organize data and eliminate duplication. In MongoDB, “denormalization” is encouraged. You actively repeat data and a single document could contain all the information it requires.
*   **Joins:** SQL provides a JOIN operator so data can be retrieved from multiple normalized tables in a single query. Joining was not possible in MongoDB until version 3.6 and limitations remain. This is another reason why data should be denormalized into self-contained documents.
*   **Transactions:** When an update changes two or more values on a single document, MongoDB ensures they all succeed or they all fail. Updates across two or more documents must be wrapped in a transaction. MongoDB has supported transactions since version 4.0 but a multi-server replica set or sharded cluster is required. The example installations below use a single server so transactions are not possible.

How To Install MongoDB[](#how-to-install-mongodb)
-------------------------------------------------

You have three options for using MongoDB on your local machine. We’ll walk you through each one.

### 1\. Use Docker (Recommended)[](#1-use-docker-recommended)

[Docker](https://www.docker.com/) is a software management tool that can install, configure, and run MongoDB or any other application in minutes.

[Install Docker and Docker Compose](https://dockerwebdev.com/tutorials/install-docker/) then create a project folder with a single file named docker-compose.yml containing the following content (note that indentions are essential):

    version: '3'
    
    services:
    
      mongodb:
        image: mongo:5
        environment:
          - MONGO_INITDB_ROOT_USERNAME=root
          - MONGO_INITDB_ROOT_PASSWORD=pass
          - MONGO_INITDB_DATABASE=mongodemo
        container_name: mongodb
        volumes:
          - dbdata:/data/db
        ports:
          - "27017:27017"
    
      adminer:
        image: dehy/adminer
        container_name: adminer
        depends_on:
          - mongodb
        ports:
          - "8080:80"
    
    volumes:
      dbdata:

Access the folder from the command line and run:

    docker-compose up

The latest version of MongoDB 5 will be downloaded and launched. This will take a few minutes on the first launch, but subsequent runs are considerably faster.

Note that:

*   A MongoDB administrator account is defined with the ID “root” and password “pass”.
*   Data is saved between restarts in a Docker volume named dbdata.
*   The Adminer database client is also provided.

You can use any MongoDB database client to connect to localhost:27017 using the ID “root” and password “pass”. Alternatively, you can access Adminer at [http://localhost:8080/](http://localhost:8080/) and log in with the following credentials:

*   **System:** MongoDB (alpha)
*   **Server:** host.docker.internal
*   **Username:** root
*   **Password:** pass

### Info[](#info)

The server host.docker.internal will work on Mac and Windows devices running Docker Desktop. Linux users should use the device’s network IP address, not localhost (Adminer resolves that to its own Docker container).

Adminer allows you to inspect collections and documents. Be aware, however, that collections are referred to as “tables”:

To run commands, you can use the MongoDB Shell (`mongosh`) or the legacy `mongo` command line REPL (Read Eval Print Loop) environment.

Access the Docker MongoDB container’s bash shell:

    docker exec -it mongodb bash

Then launch the MongoDB shell with the ID and password:

    mongosh -u root -p pass

(The legacy `mongo` command can be used if you prefer.)

You can then issue MongoDB commands like the following:

*   **`show dbs;`** — Show all databases
*   **`use mongodemo;`** — Use a specific database
*   **`show collections;`** — List collections in a database
*   **`db.person.find();`** — List all documents in a collection
*   **`exit;`** — Exit/close the shell

Shut down MongoDB by running the following command from the project directory:

    docker-compose down

### 2\. Use a Cloud Provider (No Installation)[](#2-use-a-cloud-provider-no-installation)

You could use a hosted MongoDB instance so there’s no need to install anything locally. An internet connection is essential and the speed of response will depend on the host and your bandwidth. Most services will charge a monthly and/or Megabyte usage fee.

The host will normally provide details so you can remotely administer the database using MongoDB client software.

### 3\. Install MongoDB Locally[](#3-install-mongodb-locally)

MongoDB can be installed and configured on Linux, Windows, or Mac OS. Two editions are available:

1.  A commercial Enterprise Edition
2.  An open source Community Edition (used in this tutorial)

The [MongoDB installation page](https://www.mongodb.com/docs/manual/installation/) provides instructions for various operating systems. In general:

*   Linux editions are installed using a package manager such as [apt on Ubuntu](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/)
*   [Mac OS editions are installed using brew](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/)
*   [Windows editions are installed using a .msi installer](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-windows/)

Be sure to follow the instructions carefully so your installation is successful!

How To Access Your MongoDB Database[](#how-to-access-your-mongodb-database)
---------------------------------------------------------------------------

Now that your MongoDB database is installed, it’s time to learn how to manage it. Let’s discuss what you’ll need to do in order to access and work with your database.

### 1\. Install a MongoDB Client[](#1-install-a-mongodb-client)

A MongoDB client application is required to administer databases. If you’re using a cloud or local installation, we recommend you [install the command line mongosh MongoDB Shell](https://www.mongodb.com/docs/mongodb-shell/install/).

[Adminer](https://www.adminer.org/) is a web-based database client which supports MongoDB, though it is currently limited to inspecting collections. Adminer is downloadable as a single PHP script, but it’s already set up if you use the [Docker installation](https://docs.google.com/document/d/13hLswY74cFDedN7DoUWbIshf6K7wRI4myCvKcpvNIZ0/edit#heading=h.jv0yfv8fhy7q).

A GUI client application provides a better interface for updating and inspecting data. There are several options available, including the free and cross-platform [MongoDB Compass](https://www.mongodb.com/products/compass):

[Studio 3T](https://studio3t.com/), another GUI contender, provides a commercial application that grants limited functionality for free:

You can access your MongoDB database with one of these tools by using any of the following:

1.  The machine network name, URL, or IP address (**localhost** for a local installation).
2.  The MongoDB port (**27017** by default).
3.  A user **ID** and a **password**. A root user is normally defined during installation.

### 2\. Set and Save Database Access Credentials[](#2-set-and-save-database-access-credentials)

The root administrator has unrestricted access to all databases. In general, you should use a custom user with specific privileges to limit access and increase security.

For example, the following command creates a user named **myuser** with the password **mypass** who has read and write access to the **mydb** database:

    use mydb;
    
    db.createUser({
      user: "myuser",
      pwd: "mypass",
      roles: [
        { role: "readWrite", db: "mydb" }
      ]
    });

How To Insert New Documents in MongoDB[](#how-to-insert-new-documents-in-mongodb)
---------------------------------------------------------------------------------

There is no need to define a database or a collection before inserting your first document. Using any MongoDB client, simply switch to a database named mongodemo:

    use mongodemo;

Then insert a single document into a new person collection:

    db.person.insertOne(
      {
        name: 'Abdul',
        company: 'Alpha Inc',
        telephone: [
          { home: '0123456789' },
          { work: '9876543210' }
        ]
      }
    );

View the document by running a query to return all results from the person collection:

    db.person.find({});

The result will be something like this:

    {
      "_id" : ObjectId("62442429854636a03f6b8534"),
      name: 'Abdul',
      company: 'Alpha Inc',
      telephone: [
        { home: '0123456789' },
        { work: '9876543210' }
      ]
    }

### How To Insert Multiple Documents[](#how-to-insert-multiple-documents)

You can insert multiple documents into a collection by passing an array to [insertMany()](https://www.mongodb.com/docs/manual/reference/method/db.collection.insertMany/). The following code creates additional person documents and a new company collection:

    db.person.insertMany([
      {
        name: 'Brian',
        company: 'Beta Inc'
      },
      {
        name: 'Claire',
        company: 'Gamma Inc',
        telephone: [
          { cell: '3141592654' }
        ]
      },
      {
        name: 'Dawn',
        company: 'Alpha Inc'
      },
      {
        name: 'Esther',
        company: 'Beta Inc',
        telephone: [
          { home: '001122334455' }
        ]
      },
      {
        name: 'George',
        company: 'Gamma Inc'
      },
      {
        name: 'Henry',
        company: 'Alpha Inc',
        telephone: [
          { work: '012301230123' },
          { cell: '161803398875' }
        ]
      },
    ]);
    
    db.company.insertMany([
      {
        name: 'Alpha Inc',
        base: 'US'
      },
      {
        name: 'Beta Inc',
        base: 'US'
      },
      {
        name: 'Gamma Inc',
        base: 'GB'
      },
    ]);

### Where Does \_id Come From?[](#where-does-_id-come-from)

MongoDB automatically assigns an \_id to every document in a collection. This is an ObjectID — a BSON (Binary Javascript Object Notation) value containing:

*   The Unix epoch in seconds at the point of creation (4 bytes)
*   A 5-byte machine/process ID
*   A 3-byte counter starting with a random value

This is the document’s primary key. The 24-character hexadecimal value is guaranteed to be unique across all documents in the database, and it cannot be changed once inserted.

MongoDB also provides a [getTimeStamp() function](https://www.mongodb.com/docs/manual/reference/method/ObjectId.getTimestamp/) so you can obtain the document’s creation date/time without having to explicitly set a value. Alternatively, you can define your own unique \_id value when a document is created.

### Data Denormalization[](#data-denormalization)

The records inserted above set each user’s company to a string such as “Alpha Inc”. This is not recommended in normalized SQL databases:

*   It’s easy to make a mistake: one user is assigned to “Alpha Inc” while another is “Alpha Inc.” (additional period character). They are treated as different companies.
*   Updating a company name could mean updating many records.

The SQL solution is to create a _company_ table and associate a company to a person using its primary key (probably an integer). The key would remain the same regardless of company name changes and the database can enforce rules to guarantee data integrity.

Denormalization is encouraged in MongoDB. You should actively repeat data and a single document could contain all the information it requires. This has a several advantages:

*   Documents are self-contained and easier to read — there’s no need to reference other collections.
*   Write performance can be faster than a SQL database because fewer data integrity rules are enforced.
*   Sharding — or distributing data across multiple machines — becomes easier because it is not necessary to reference data in other collections.

Simple MongoDB Queries[](#simple-mongodb-queries)
-------------------------------------------------

You can list all documents in a collection, such as person, by using an empty find():

    db.person.find({})

The [count() method](https://www.mongodb.com/docs/manual/reference/command/count/) returns the number of documents (in our case, that number will be 7):

    db.person.find({}).count();

A [sort() method](https://www.mongodb.com/docs/manual/reference/operator/update/sort/) returns the documents in any order you prefer such as by name in reverse alphabetical order:

    db.person.find({}).sort({ name: -1 });

You can also limit the number of documents returned, e.g. find the first three names:

    db.person.find({}).sort({ name: 1 }).limit(2);

You can search for specific records by defining a query with one or more fields, e.g. locate all person documents where the name is set to “Claire”:

    db.person.find({ name: 'Claire' });

[Logical operators](https://www.mongodb.com/docs/manual/reference/operator/query/) such as $and, $or, $not, $gt (greater than), $lt (less than), and $ne (not equal), are also supported, e.g. locate all person documents where the company is either “Alpha Inc” or “Beta Inc”:

    db.person.find({
      $or: [
        { company: 'Alpha Inc' },
        { company: 'Beta Inc' }
      ]
    });

In the example database, the same result could be achieved with $nin (not in) to extract all documents where the company is **not** “Gamma Inc”:

    db.person.find({
      company: { $nin: ['Gamma Inc'] }
    });

A second value object in the find() method sets a _projection_ which defines the returned fields. In this example, just the name is returned (note the document \_id is always returned unless it’s explicitly switched off):

    db.person.find(
      { name:'Claire' },
      { _id:0, name:1 }
    );

The result:

    {
      "name" : "Claire"
    }

The [$elemMatch query](https://www.mongodb.com/docs/manual/reference/operator/query/elemMatch/) allows you to find items in an array, such as all documents where the telephone array has a work item. The same $elemMatch can be used in the projection to show the work number only:

    db.person.find(
      {
        telephone: { $elemMatch: { work: { $exists: true }} }
      },
      {
        _id: 0,
        name:1,
        telephone: { $elemMatch: { work: { $exists: true }}}
      }
    );

The result:

    {
      "name" : "Abdul",
      "telephone" : [
        { "work" : "9876543210" }
      ]
    },
    {
      "name" : "Henry",
      "telephone" : [
        { "work" : "012301230123" }
      ]
    }

Using Cursors in MongoDB[](#using-cursors-in-mongodb)
-----------------------------------------------------

Most database drivers allow the results from a query to be returned as an array or similar data structure. However, if that set contains thousands of documents, this could lead to memory issues.

Like most SQL databases, MongoDB supports the concept of [cursors](https://www.mongodb.com/docs/manual/reference/method/js-cursor/). Cursors allow an application to read query results one at a time before proceeding to the next item or abandoning the search.

Cursors can also be used from a MongoDB shell:

    let myCursor = db.person.find( {} );
    
    while ( myCursor.hasNext() ) {
      print(tojson( myCursor.next() ));
    }

How To Create Indexes in MongoDB[](#how-to-create-indexes-in-mongodb)
---------------------------------------------------------------------

The person collection currently holds seven documents so any query will not be computationally expensive. However, imagine you have one million contacts with a name and email address. Contacts may be ordered by name but email addresses will be in a seemingly random order.

If you need to look up a contact by their email, the database would have to search up to one million items before it finds a match. Adding an index on the email field creates a lookup “table” where emails are stored in alphabetical order. The database can now use more efficient search algorithms to locate the correct person.

Indexes become essential as the number of documents increases. In general, you should apply an index to any field which could be referenced in a query. You _could_ apply indexes to every field, but be aware that this would slow data updates and increase the disk space required because re-indexing becomes necessary.

MongoDB offers a range of index types.

### Single Field Indexes[](#single-field-indexes)

Most indexes will be applied to single fields, e.g. index the name field in ascending alphabetical order:

    db.person.createIndex({ name: 1 });

Using -1 reverses the order. That would be of little benefit in our example here, but it could be practical if you have a date field where more recent events take priority.

Three other indexes are useful in the example mongodemo database:

    db.person.createIndex( { company: 1 } );
    db.company.createIndex( { name: 1 } );
    db.company.createIndex( { base: 1 } );

### Compound Indexes on Multiple Fields[](#compound-indexes-on-multiple-fields)

Two or more fields can be specified in an index, e.g.

    db.person.createIndex( { name: 1, company: 1 } );

This can be useful when a field is regularly used in conjunction with another in search queries.

### Multikey Indexes on Array or Object Elements[](#multikey-indexes-on-array-or-object-elements)

Documents can be complex and it’s often necessary to index fields deeper in the structure, such as the work telephone number:

    db.products.createIndex( { 'telephone.work': 1 } );

### Wildcard Indexes[](#wildcard-indexes)

A wildcard can index every field in a document. This is generally practical on smaller and simpler documents which could be queried in a variety of ways:

    db.company.createIndex( { '$**': 1 } );

### Fulltext Indexes[](#fulltext-indexes)

A text index allows you to create search-engine-like queries that can examine text across all string fields and order by relevance. You can limit the text index to specific fields:

    db.person.createIndex( { name: "text", company: "text" } );

…or create a text index on all string fields:

    db.person.createIndex( { "$**": "text" } );

The [$text operator](https://www.mongodb.com/docs/manual/text-search/) allows you to search this index, such as finding all documents where “Gamma” is referenced:

    db.person.find({ $text: { $search: 'Gamma' } });

Note that full text searches generally require five or more characters to return useful results.

### Other Index Types[](#other-index-types)

MongoDB provides several other specialized index types:

*   [hashed index](https://www.mongodb.com/docs/manual/core/index-hashed/)
*   [2d index](https://www.mongodb.com/docs/manual/core/2dsphere/) — points on a two-dimensional plane
*   [2dsphere index](https://www.mongodb.com/docs/manual/core/2d/) — geometries on an Earth-like sphere

How To Manage MongoDB Indexes[](#how-to-manage-mongodb-indexes)
---------------------------------------------------------------

The indexes defined on a collection can be examined with:

    db.person.getIndexes();

This returns an array of results such as:

    [
      {
        "v" : 2.0,
        "key" : { "_id" : 1.0 },
        "name" : "_id_"
      },
      {
        "v" : 2.0,
        "key" : { "company" : 1.0 },
        "name" : "company_1"
      },
      {
        "v" : 2.0,
        "key" : { "name" : 1.0 },
        "name" : "name_1"
      }
    ]

The “key” defines the field and order while “name” is a unique identifier for that index — such as “company\_1” for the index on the company field.

The effectiveness of an index can be examined by adding an [.explain() method](https://www.mongodb.com/docs/manual/reference/method/db.collection.explain/) to any query, e.g.

    db.person.find({ name:'Claire' }).explain();

This returns a large set of data but the “winningPlan” object shows the “indexName” used in the query:

    "winningPlan" : {
      "stage" : "FETCH",
      "inputStage" : {
        "stage" : "IXSCAN",
        "keyPattern" : { "name" : 1.0 },
        "indexName" : "name_1",
      }
    }

If necessary, you can drop an index by referencing its name:

    db.person.dropIndex( 'name_1' );

or using the index specification document:

    db.person.dropIndex({ name: 1 });

The [dropIndexes() method](https://www.mongodb.com/docs/manual/reference/method/db.collection.dropIndexes/) allows you to drop more than one index in a single command.

Using MongoDB Data Validation Schemas[](#using-mongodb-data-validation-schemas)
-------------------------------------------------------------------------------

Unlike SQL, data definition schemas are not necessary in MongoDB. You can post any data to any document in any collection at any time.

This provides considerable freedom. However, there may be times when you want to insist that rules are followed. For example, it should not be possible to insert a document into the person collection unless it contains a name.

Validation rules can be specified using a [$jsonSchema object](https://www.mongodb.com/docs/manual/reference/operator/query/jsonSchema/) which defines an array of required items and the properties of each validated field. The person collection has already been created, but you can still define a schema which specifies that a name string is required:

    db.runCommand({
      collMod: 'person',
      validator: {
        $jsonSchema: {
          required: [ 'name' ],
          properties: {
            name: {
              bsonType: 'string',
              description: 'name string required'
            }
          }
        }
      }
    });

Try inserting a person document without a name:

    db.person.insertOne({ company: 'Alpha Inc' });

…and the command will fail:

    {
      "index" : 0.0,
      "code" : 121.0,
      "errmsg" : "Document failed validation",
      "op" : {
          "_id" : ObjectId("624591771658cd08f8290401"),
          "company" : "Alpha Inc"
      }
    }

Schemas can also be defined if you [create a collection](https://www.mongodb.com/docs/manual/reference/method/db.createCollection/) before it’s used. The following command implements the same rules as above:

    db.createCollection('person', {
      validator: {
        $jsonSchema: {
            required: [ 'name' ],
            properties: {
              name: {
              bsonType: 'string',
              description: 'name string required'
              }
          }
        }
      }
    });

This more complex example creates a user collection that validates that a name, email address, and at least one telephone number must be provided:

    db.createCollection('users', {
      validator: {
        $jsonSchema: {
          required: [ 'name', 'email', 'telephone' ],
          properties: {
            name: {
              bsonType: 'string',
              description: 'name string required'
              },
              email: {
            bsonType: 'string',
              pattern: '^.+\@.+$',
              description: 'valid email required'
              },
            telephone: {
              bsonType: 'array',
              minItems: 1,
              description: 'at least one telephone number required'
              }
          }
        }
      }
    });

How To Update Existing Documents in MongoDB[](#how-to-update-existing-documents-in-mongodb)
-------------------------------------------------------------------------------------------

MongoDB offers several [update methods](https://www.mongodb.com/docs/manual/reference/update-methods/) including `updateOne()`, `updateMany()`, and `replaceOne()`. These are passed:

*   A filter object which locates documents to update
*   An update object — or an array of update objects — describing the data to change
*   An optional options object. The most useful property is upsert which can insert a new document if none is found.

The following example updates the person document where the name is set to “Henry”. It removes the work telephone number, adds a home telephone number, and sets a new birthdate:

    db.person.updateOne(
      { name: 'Henry' },
      [
        { $unset: [ 'telephone.work' ] },
        { $set: {
          'birthdate': new ISODate('1980-01-01'),
          'telephone': [ { 'home': '789789789' } ]
        } }
      ]
    );

This next example updates the person document where the name is set to “Ian”. That name does not currently exist, but setting upsert to “true” creates it:

    db.person.updateOne(
      { name: 'Ian' },
      { $set: { company: 'Beta Inc' } },
      { upsert: true }
    );

You can run query commands to examine the data updates at any time.

How To Delete Documents in MongoDB[](#how-to-delete-documents-in-mongodb)
-------------------------------------------------------------------------

The update example above used $unset to remove the work telephone number from the document with the name “Henry”. To remove a whole document, you can use one of several [deletion methods](https://www.mongodb.com/docs/manual/reference/delete-methods/) including `deleteOne()`, `deleteMany()`, and `remove()` (which can delete one or many).

The newly created document for Ian can be deleted with an appropriate filter:

    db.person.deleteOne({ name: 'Ian' });

Using Aggregation Operations in MongoDB[](#using-aggregation-operations-in-mongodb)
-----------------------------------------------------------------------------------

[Aggregation](https://www.mongodb.com/docs/manual/aggregation/) is powerful but can be difficult to comprehend. It defines a series — or _pipeline_ — of operations in an array. Each stage of that pipeline [performs an operation](https://www.mongodb.com/docs/manual/meta/aggregation-quick-reference/) such as filtering, grouping, calculating, or modifying a set of documents. A stage can also use SQL JOIN-like behavior with a [$lookup operation](https://www.mongodb.com/docs/manual/reference/operator/aggregation/lookup/). The resulting documents are passed to the next stage of the pipeline for further processing as necessary.

Aggregation is best illustrated with an example. We will build a query step by step which returns the name, company, and work telephone number (if available) of anyone who works for an organization based in the US.

The first operation runs a $match to filter US-based companies:

    db.company.aggregate([
      { $match: { base: 'US' } }
    ]);

This returns:

    {
      "_id" : ObjectId("62442429854636a03f6b853b"),
      "name" : "Alpha Inc",
      "base" : "US"
    }
    {
      "_id" : ObjectId("62442429854636a03f6b853c"),
      "name" : "Beta Inc",
      "base" : "US"
    }

We can then add a new $lookup pipeline operator which matches the company name (localField) to the company (foreignField) in the person (from) collection. The output will be appended as an employee array to each company’s document:

    db.company.aggregate([
      { $match: { base: 'US' } },
      { $lookup: {
          from: 'person',
          localField: 'name',
          foreignField: 'company',
                as: 'employee'
              }
            }
    ]);

And here’s the result:

    {
      "_id" : ObjectId("62442429854636a03f6b853b"),
      "name" : "Alpha Inc",
      "base" : "US",
      "employee" : [
        {
          "_id" : ObjectId("62442429854636a03f6b8534"),
          "name" : "Abdul",
          "company" : "Alpha Inc",
          "telephone" : [
            { "home" : "0123456789" },
            { "work" : "9876543210" }
          ]
        },
        {
          "_id" : ObjectId("62442429854636a03f6b8537"),
          "name" : "Dawn",
          "company" : "Alpha Inc"
        },
        {
          "_id" : ObjectId("62442429854636a03f6b853a"),
          "name" : "Henry",
          "company" : "Alpha Inc",
          "telephone" : [
            { "home" : "789789789" }
          ],
        }
      ]
    }
    {
      "_id" : ObjectId("62442429854636a03f6b853c"),
      "name" : "Beta Inc",
      "base" : "US",
      "employee" : [
        {
          "_id" : ObjectId("62442429854636a03f6b8535"),
          "name" : "Brian",
          "company" : "Beta Inc"
        },
        {
          "_id" : ObjectId("62442429854636a03f6b8538"),
          "name" : "Esther",
          "company" : "Beta Inc",
          "telephone" : [
           { "home" : "001122334455" }
          ]
        }
      ]
    }

A [$project (projection) operation](https://www.mongodb.com/docs/manual/reference/operator/aggregation/project/#mongodb-pipeline-pipe.-project) can now remove all but the employee arrays. This is followed by an [$unwind operation](https://www.mongodb.com/docs/manual/reference/operator/aggregation/unwind/#mongodb-pipeline-pipe.-unwind) to destruct the array and obtain separate employee documents:

    db.company.aggregate([
      { $match: { base: 'US' } },
      { $lookup: { from: 'person', localField: 'name', foreignField: 'company', as: 'employee' } },
      { $project: { _id: 0, employee: 1 } },
      { $unwind: '$employee' }
    ]);

The result:

    {
      "employee" : {
        "_id" : ObjectId("62442429854636a03f6b8534"),
        "name" : "Abdul",
        "company" : "Alpha Inc",
        "telephone" : [
          { "home" : "0123456789" },
          { "work" : "9876543210" }
        ]
      }
    }
    {
      "employee" : {
        "_id" : ObjectId("62442429854636a03f6b8537"),
        "name" : "Dawn",
        "company" : "Alpha Inc"
      }
    }
    {
      "employee" : {
        "_id" : ObjectId("62442429854636a03f6b853a"),
        "name" : "Henry",
        "company" : "Alpha Inc",
        "telephone" : [
          { "home" : "789789789" }
        ]
      }
    }
    {
      "employee" : {
        "_id" : ObjectId("62442429854636a03f6b8535"),
        "name" : "Brian",
        "company" : "Beta Inc"
      }
    }
    {
      "employee" : {
        "_id" : ObjectId("62442429854636a03f6b8538"),
        "name" : "Esther",
        "company" : "Beta Inc",
        "telephone" : [
          { "home" : "001122334455" }
        ]
      }
    }

Finally, an [$replaceRoot operation](https://www.mongodb.com/docs/manual/reference/operator/aggregation/replaceRoot/#mongodb-pipeline-pipe.-replaceRoot) is used to format each document so just the person’s name, company, and work telephone number is returned. This is followed by a [$sort](https://www.mongodb.com/docs/manual/reference/operator/aggregation/sort/#mongodb-pipeline-pipe.-sort) to output documents in ascending name order. The full aggregate query:

    db.company.aggregate([
      { $match: { base: 'US' } },
      { $lookup: { from: 'person', localField: 'name', foreignField: 'company', as: 'employee' } },
      { $project: { _id: 0, employee: 1 } },
      { $unwind: '$employee' },
      { $replaceRoot: {
        newRoot: {
          $mergeObjects: [ {
            name: "$employee.name",
            company: '$employee.company',
            work: { $first: '$employee.telephone.work' }
          }, "$name" ]
       } } },
      { $sort: { name: 1 } }
    ]);

The result:

    {
      "name" : "Abdul",
      "company" : "Alpha Inc",
      "work" : "9876543210"
    }
    {
      "name" : "Brian",
      "company" : "Beta Inc",
    }
    {
      "name" : "Dawn",
      "company" : "Alpha Inc",
    }
    {
      "name" : "Esther",
      "company" : "Beta Inc"
    }
    {
      "name" : "Henry",
      "company" : "Alpha Inc"
    }

There are other ways to achieve this result, but the key point is that MongoDB can do the bulk of the work. It’s rarely necessary to read documents and manipulate the data in your application code directly.

How To Run Bulk MongoDB Operations[](#how-to-run-bulk-mongodb-operations)
-------------------------------------------------------------------------

By default, MongoDB can handle 1,000 concurrent operations. This is unlikely to be a problem while using mongosh, but applications can reach this limit if they make a series of data manipulations on individual records. Node.js applications are especially problematic because they can rapidly issue a series of asynchronous requests without having to wait until they’ve completed.

To circumvent this issue, MongoDB provides a [bulk operations API](https://www.mongodb.com/docs/manual/reference/method/js-bulk/) which accepts any number of updates that can be executed in order or in any order.

Here’s a pseudocode](/kba/what-is-pseudocode/) example in Node.js:

    // reference the mycollection collection
    const bulk = db.collection('mycollection').initializeUnorderedBulkOp();
    
    // make any number of data changes
    bulk.insertOne(...);
    bulk.insertMany(...)
    bulk.updateOne(...);
    bulk.deleteOne(...);
    // etc...
    
    bulk.execute();

The last statement effectively issues a single MongoDB request so you have less chance of hitting that 1,000 operations limit.  

Summary[](#summary)
-------------------

MongoDB provides a flexible store for applications such as content management systems, address books, and social networks where strict data structures are too rigid and difficult to define. Data writes are fast and sharding across multiple servers becomes easier.

Writing applications using a MongoDB database can also be liberating. It’s possible to store any data in any document in any collection at any time. This is especially practical when you’re developing a prototype or Minimum Viable Product using agile methodologies where requirements evolve over time.

That said, complex queries can be a challenge and denormalization concepts are difficult to accept when you’re migrating from the SQL world.

MongoDB is less suited to applications which have strict transactional requirements where data integrity is essential, such as with banking, accounting, and stock control systems. These have identifiable data fields which should be designed before coding commences.

There are plenty of application types between these two extremes so choosing an appropriate database becomes more difficult. Fortunately, NoSQL databases including MongoDB have started to adopt SQL-like options including JOINs and transactions.

Conversely, SQL databases such as MySQL and PostgreSQL now offer NoSQL-like JSON data fields. They too may warrant your attention, but as always, the final choice is yours.
