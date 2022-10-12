# Database-Management-System


# Creating Student Database in MongoDB

## Pre-requisites
 
###  Install MongoDB and mongoose in your project.
### Spin up your mongo server and your mongo shell in the terminal.

## Steps

1. ### Step 1: Require Mongoose in your project
const mongoose= require(“mongoose”);

2. ### Step 2: Connect your app with a MongoDB database using the URL where your MongoDB is hosted locally.
 mongoose.connect('mongodb://localhost:27017/Student', { useNewUrlParser : true });

3. ### Step 3: Create a new schema “studentsSchema”
const studentsSchema={  
  name:String,  
  id: Number   
};

4. ### Step 4: Create a new mongoose model based on this schema using the singular form of your collection i.e. student, and the schema
const Item=mongoose.model(" Student ", studentsSchema);

5. ### Step 5: Create a new mongoose document using your Student model
const student1=new Student({  
  name : " Stu-1 ",  
  id: 1  
});

6. ### Step 6: Save that document to your database
student1.save(function (err, student) {  
      if (err) return console.error(err);  
      });

## Ta-daa, you have now created a Student Database with data in it :tada: :tada:






