# MongoDB CRUD Application (Node.js)

This project is a simple backend demonstration showing how to connect a Node.js application to **MongoDB Atlas** and perform basic **CRUD operations** — Create, Read, Update, and Delete.

It is intended for beginners who want to understand how MongoDB works, how cloud databases are connected, and how data is managed using Node.js.

This is a **backend-only project** and does not include any frontend interface.

---

## Project Description

In this project, you will learn:
- How to create and configure a MongoDB Atlas cluster
- How to connect MongoDB Atlas with a Node.js application
- How to insert, fetch, update, and delete documents
- How to use async/await for database operations
- How a simple backend project is structured

---

## Technologies Used

- **Node.js** – JavaScript runtime environment
- **MongoDB Atlas** – Cloud-hosted MongoDB database
- **MongoDB Node.js Driver** – Official MongoDB driver
- **JavaScript (ES6)** – Backend logic

---
## FILE DIRECTORY

mongodb-crud/
│
├── index.js # Main application file
├── package.json # Project metadata and dependencies
├── node_modules/ # Installed npm packages
└── README.md

---

## MongoDB Atlas Setup Guide

### Step 1: Create an Atlas Account
1. Visit https://www.mongodb.com/atlas
2. Sign up using email or Google
3. Log in to the MongoDB Atlas dashboard

---

### Step 2: Create a Free Cluster
1. Click **Create Cluster**
2. Select **Shared (Free Tier)**
3. Choose a cloud provider (AWS preferred)
4. Select the nearest region
5. Create the cluster

---

### Step 3: Create a Database User
1. Open **Database Access**
2. Click **Add New Database User**
3. Set a username and password
4. Grant **Read and Write** access
5. Save the user

---

### Step 4: Allow Network Access
1. Go to **Network Access**
2. Click **Add IP Address**
3. Allow access from anywhere (for testing)
4. Confirm changes

---

### Step 5: Get the Connection String
1. Open **Clusters**
2. Click **Connect**
3. Choose **Connect your application**
4. Copy the MongoDB URI

Example:

## Project Files
mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/



Replace the placeholders with your credentials.

---

## Updating the Connection URI

In `index.js`, replace:

```js
const uri = "YOUR_MONGODB_URI";
```
With:
      ``` const uri = "mongodb+srv://username:password@cluster0.xxxxx.mongodb.net/";```


## CRUD Operations Explained
Connecting to MongoDB
await client.connect();
console.log("Database connected successfully");

## Create (Insert Data)
await students.insertOne({ name: "Alex", age: 21, marks: 85 });

## Read (Fetch Data)
const data = await students.find().toArray();

## Update (Modify Data)
await students.updateOne(
  { name: "Alex" },
  { $set: { marks: 90 } }
);

## Delete (Remove Data)
await students.deleteOne({ name: "Alex" });

## Running the Project Locally
Step 1: Create Project Folder
mkdir mongodb-crud
cd mongodb-crud

Step 2: Initialize Node.js Project
npm init -y

Step 3: Install MongoDB Driver
npm install mongodb

Step 4: Run the Application
node index.js

## Example Output
Connected to MongoDB Atlas
Document inserted successfully
Fetched documents from collection
Document updated
Database connection closed

## What You Will Learn

Setting up MongoDB Atlas

Connecting Node.js to a cloud database

Performing CRUD operations

Using async/await for database handling

Writing clean backend demo code

## Disclaimer

This project is created strictly for educational purposes.
Do not share or expose your MongoDB credentials publicly.
