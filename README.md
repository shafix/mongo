# mongo
MongoDB

## Update data type of a certain document field
```js
db.getCollection('Applications-PROD').find({ _id : "SL-FIA-18408182" }).forEach(function(obj) { 
    obj.sentTimestamp = new NumberLong(obj.sentTimestamp);
    db.getCollection('Applications-PROD').save(obj);
});
```
