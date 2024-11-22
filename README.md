<img src="https://socialify.git.ci/Nokwanda2000/Mongo-Databases/image?language=1&owner=1&name=1&stargazers=1&theme=Light" alt="Mongo-Databases" width="640" height="320" />

<h1>Mongo-Databases</h1>



<p>This document provides step-by-step instructions for using the MongoDB shell (mongosh) to complete the following tasks</p>

Starting the MongoDB shell

Creating databases and collections

Inserting documents

Exporting the database

Starting the MongoDB Shell (mongosh)

Open a terminal or command prompt.


## Run Locally
Clone the project
```bash
  git clone https://github.com/Amniei/Shopping-List.git
```


## Start the MongoDB shell by typing:
```bash
mongosh
```
## If the MongoDB server is running on a non-default host or port, specify the connection string. For example:
```bash
mongosh "mongodb://localhost:27017"
```
## MongoDB Commands

`1. Create a Database`

## Switch to the desired database
```bash
use Codetribe
```
`2. Create Collections and Insert Documents`

a. Facilitators Collection:

Insert a document with the fields Name, Location, and Course:

db.Facilitators.insertOne({
  Name: "John Doe",
  Location: "Cape Town",
  Course: "Web Development"
})

b. Trainees Collection:

Insert a document with the fields Name, Location, and Facilitator:

db.Trainees.insertOne({
  Name: "Jane Smith",
  Location: "Johannesburg",
  Facilitator: "John Doe"
})

c. Projects Collection:

Insert a document with the fields Name, Course, and Lesson:

db.Projects.insertOne({
  Name: "Node.js Basics",
  Course: "Backend Development",
  Lesson: "Introduction to Node.js"
})

`3. Verify Inserted Documents`

To confirm the documents were inserted, use the find() command:

a. Facilitators:

db.Facilitators.find().pretty()

b. Trainees:

db.Trainees.find().pretty()

c. Projects:

db.Projects.find().pretty()

`4. Export the Database`

To export the database, use the mongodump command. Ensure MongoDB tools are installed and added to your system's PATH.

Open a terminal or command prompt.

`Run the following command:`

mongodump --db=Codetribe --out=./Codetribe_Dump

This creates a folder named Codetribe_Dump containing the exported data.

Additional Notes

Ensure the MongoDB server is running before starting the shell or using export commands.

If mongodump is not recognized, ensure MongoDB Database Tools are installed and added to the PATH.

## Troubleshooting

MongoDB Shell Connection Error:

Verify the MongoDB server is running.

Check the connection string for accuracy.

mongodump Not Recognized:

Ensure MongoDB tools are installed.

Add the tools’ bin directory to the system PATH.

By following the steps above, you can successfully create databases, collections, and documents using the MongoDB shell, and export your database for backup or sharing.

