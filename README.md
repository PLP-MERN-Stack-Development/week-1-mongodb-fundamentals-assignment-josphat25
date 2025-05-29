[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19649481&assignment_repo_type=AssignmentRepo)
# MongoDB Fundamentals Assignment

This assignment focuses on learning MongoDB fundamentals including setup, CRUD operations, advanced queries, aggregation pipelines, and indexing.
## answer
# CRUD Operations:

insertOne() and insertMany()

find(), findOne(), updateOne(), deleteOne()

# Advanced Queries:

Filtering with comparison operators ($gt, $lt, etc.)

Projection to return specific fields

Sorting (sort()), limiting (limit())

# Aggregation Pipelines:

$match, $group, $sort, $project

db.books.aggregate([

  { $match: { genre: "Fiction" } },
  
  { $group: { _id: "$author", count: { $sum: 1 } } }
  
])

# Indexing:

db.books.createIndex({ title: 1 })


## Assignment Overview

You will:
1. Set up a MongoDB database
2. Perform basic CRUD operations
3. Write advanced queries with filtering, projection, and sorting
4. Create aggregation pipelines for data analysis
5. Implement indexing for performance optimization

## Getting Started

1. Accept the GitHub Classroom assignment invitation
2. Clone your personal repository that was created by GitHub Classroom
3. Install MongoDB locally or set up a MongoDB Atlas account
4. Run the provided `insert_books.js` script to populate your database
5. Complete the tasks in the assignment document

## Files Included

- `Week1-Assignment.md`: Detailed assignment instructions
- `insert_books.js`: Script to populate your MongoDB database with sample book data

## Requirements

- Node.js (v18 or higher)
- MongoDB (local installation or Atlas account)
- MongoDB Shell (mongosh) or MongoDB Compass

## Submission

Your work will be automatically submitted when you push to your GitHub Classroom repository. Make sure to:

1. Complete all tasks in the assignment
2. Add your `queries.js` file with all required MongoDB queries
3. Include a screenshot of your MongoDB database
4. Update the README.md with your specific setup instructions

## answer 

// Insert

db.books.insertOne({ title: "Mongo Basics", author: "Jane Doe" })

// Find

db.books.find({ genre: "Non-fiction" }).limit(5)

// Update

db.books.updateOne({ title: "Mongo Basics" }, { $set: { genre: "Tech" } })

// Delete

db.books.deleteOne({ author: "Unknown" })

// Aggregation

db.books.aggregate([

  { $match: { genre: "Science" } },
  
  { $group: { _id: "$author", count: { $sum: 1 } } }
  
])

// Indexing

db.books.createIndex({ author: 1 })

## Resources

- [MongoDB Documentation](https://docs.mongodb.com/)
- [MongoDB University](https://university.mongodb.com/)
- [MongoDB Node.js Driver](https://mongodb.github.io/node-mongodb-native/) 
