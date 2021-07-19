# Read
## find()
find() return a cursor 

    > db
    test
    > db.users.find()
    { "_id" : ObjectId("6064182d0c2d5f31580c7758"), "name" : "julie" }
    { "_id" : ObjectId("60639204f498d1b501bfaa39"), "name" : "jean" }
    { "_id" : ObjectId("606418130c2d5f31580c7757"), "name" : "julie" }
    { "_id" : ObjectId("606394c350a5f130c139b639"), "name" : "Lucie" }
    { "_id" : ObjectId("6068cfc4a5d41368ec129963"), "name" : "Jean" }
    { "_id" : ObjectId("6068d13a76c81a48f29dde23"), "name" : "julie", "local" : { "email" : "jean@gmail.com" } }
    { "_id" : ObjectId("6068d18f76c81a48f29dde24"), "date" : ISODate("2021-04-03T20:35:27.245Z"), "name" : "julie", "local" : { "email" : "julie@gmail.com" } }
    { "_id" : ObjectId("6068d30b76c81a48f29dde29"), "date" : ISODate("2021-04-03T20:41:47.651Z"), "name" : "julie", "local" : { "email" : "julie@gmail.com" } }
    { "_id" : ObjectId("6068d30b76c81a48f29dde2a"), "date" : ISODate("2021-04-03T20:41:47.652Z"), "name" : "julie", "local" : { "email" : "julie@gmail.com" } }

### printjson(cursor)
   
    > var cursor = db.users.find()
    > printjson(cursor)
    {
            "_mongo" : connection to 127.0.0.1:27017,
            "_db" : test,
            "_collection" : test.users,
            "_ns" : "test.users",
            "_query" : {
                    
            },
            "_fields" : null,
            "_limit" : 0,
    ...

#### cursor.count()
   
    > cursor.count()
    9
    
#### cursor.next()
    
    > cursor.next()
    { "_id" : ObjectId("6064182d0c2d5f31580c7758"), "name" : "julie" }
    > cursor.hasNext()
    true

#### cursor.pretty()

    > cursor.pretty()
      { "_id" : ObjectId("60639204f498d1b501bfaa39"), "name" : "jean" }
      { "_id" : ObjectId("606418130c2d5f31580c7757"), "name" : "julie" }
      { "_id" : ObjectId("606394c350a5f130c139b639"), "name" : "Lucie" }
      { "_id" : ObjectId("6068cfc4a5d41368ec129963"), "name" : "Jean" }
      {
              "_id" : ObjectId("6068d13a76c81a48f29dde23"),
              "name" : "julie",
              "local" : {
                      "email" : "jean@gmail.com"
              }
      }
      {
              "_id" : ObjectId("6068d18f76c81a48f29dde24"),
              "date" : ISODate("2021-04-03T20:35:27.245Z"),
              "name" : "julie",
              "local" : {
                      "email" : "julie@gmail.com"
              }
      }
      {
              "_id" : ObjectId("6068d30b76c81a48f29dde29"),
              "date" : ISODate("2021-04-03T20:41:47.651Z"),
              "name" : "julie",
              "local" : {
                      "email" : "julie@gmail.com"
              }
      }
      {
              "_id" : ObjectId("6068d30b76c81a48f29dde2a"),
              "date" : ISODate("2021-04-03T20:41:47.652Z"),
              "name" : "julie",
              "local" : {
                      "email" : "julie@gmail.com"
              }
      }
 
            
