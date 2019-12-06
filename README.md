# Enterpriseproject
my first repo
my staff collection
 db.staff.find().pretty()
{
        "_id" : ObjectId("5d8e78c85710ff3ad231102f"),
        "sid" : 100,
        "password" : "abc",
        "designation" : "event manager"
}
{
        "_id" : ObjectId("5d8e78d95710ff3ad2311030"),
        "sid" : 110,
        "password" : "abcd",
        "designation" : "event manager"
}
{
        "_id" : ObjectId("5d8e79395710ff3ad2311031"),
        "sid" : 111,
        "password" : "bcd",
        "designation" : "event manager"
}
{
        "_id" : ObjectId("5d8e795d5710ff3ad2311032"),
        "sid" : 112,
        "password" : "888cd",
        "designation" : "event supervisor"
        
}
//////SERVICES

const express= require('express');
const app = express();
var mongo= require('mongodb');
app.use(express.json());
//connect to database and show list of books.

app.get('/api/ass',(req,res)=>{
var MongoClient = require('mongodb').MongoClient;
var url = "mongodb://localhost:27017/";
MongoClient.connect(url, function(err, db) {
  if (err) throw err;
  var dbo = db.db("event_management_system");
 
  dbo.listCollections().toArray(function(err, collInfos) {
    if (err) throw err;
    console.log(collInfos);
    res.send(collInfos);
db.close();
 });
});
});
