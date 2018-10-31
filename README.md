# mongo
MongoDB

## Update data type of a certain document field
```js
db.getCollection('XXXX').find({ _id : "XXXXXXX" }).forEach(function(obj) { 
    obj.sentTimestamp = new NumberLong(obj.sentTimestamp);
    db.getCollection('XXXXX').save(obj);
});
```

## Update a field of a document
```js
db.getCollection('XXX').updateOne({ _id : "XXX" }, { $set: { "applicant.firstName" : "BLA BLA BLA" } } );
```
