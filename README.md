# Database-Management-System

## What is mapreduce in MongoDb?🍃
Let's get started with the definition and then understand how it works.😃👍

#### Definition
**mapReduce** , data processing programming model of MongoDb is mostly used for performing operations on large datasets.
mapReduce() function performs the map and the reduce operations.
To group the data in key-value pairs, map function is used and then the operations are performed using the reduce function of mapReduce to the keys with multiple values.
mapReduce result can be returned as a document or written into a collection as well.

#### Syntax

The syntax of mapReduce() function:
```
db.collectionName.mapReduce(
... map(),
...reduce(),
...query{},
...output{}
);
```
- The **map()** function has emit which takes two parameters: key and value.
- The **reduce()** function performs the operation on the mapped data. It can perform operations like avg,sum etc.
- The **query** is used to filter the result.
- The **output** specifies the collection where the result is stored.

#### Example
For instance, let's assume that we have to get the min marks from each class.\
Min marks because, not everyone get's good grades right?🥲, anyway let's get back to it...\
So, let's assume there are three keys which are id, class and marks. 
```
{"id":1, "class":C10, "marks":80}
{"id":2, "class":C10, "marks":90}
{"id":1, "class":C9, "marks":10}
{"id":1, "class":C9, "marks":20}
{"id":1, "class":C8, "marks":90}
```
We will group this data using the *class* key and the value will be *marks*.
For this let us write the map function.\
We will create a var map with emit function that shows that we are using class as key and marks as value.

```
var map = function(){emit(this.class, this.marks)};
```

The following result will be obtained by this:\
{“C10”:[80, 90]},  {“C9”:[10, 20]},  {“C8”:[90] }

Now,this isn't the end result we wanted, is it?\
So, in order to find the min marks from each  class we will use the reduce function to perform the operation.

```
var reduce = function(class,marks){return Array.min(marks);};
```
This is a reduce function, which accepts two parameters i.e. the key which is class and the value which is marks. It then filters the min marks from each class.
\
In order to get the output in a new collection we will:

```
db.collectionName.mapReduce(map,reduce,{out :"collectionName"});
```

This is how we can use the mapReduce function in MongoDb!!