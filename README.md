# Microsoft Access and Google Firebase Integration
All the tools to develop your next Microsoft Access Application which stores data in Firebase and Sync for Offline Use

##Intro##
There are many a times situation where we want to have a database which we can connect from anywhere. Here I am going to demonstrate how to achive this. We are going to use Firebase (a Google Product)

##Prerequisies##
Before you can start using tools to create MS Access Applications which Connect with Firebase, you will need knowledge of the following
  1. MS Access VBA
  2. Rest API of Firebase 
  While I will try to make all the code explanation, having knowledge of these will help you in making your apps faster.

##Broad Picture##
The Idea is to use Firebase Rest API to talk to the Firebase for `CRUD`. These api's are extremely easy to learn and use. We will be storing the data in Access tables as well as in Firebase. If you are very new to Access programming, skip this section.
###Create###
  1. Use `beforeUpdate` event on the Access Form to Hit `POST` api.
  2. Get Unique ID in response and set this as the `Record Id`
  3. Now Access will save the record
###Read###
  1. Create Refresh Button and Hit `GET` api
  2. Get data in Json
  3. Parse this Json and save it in the table
###Update###
  1. Use `beforeUpdate` event on the Access Form to Hit `PATCH` api.
  2. Now access will save the record
###Delete###
  1. Create Delete Button and Hit `DELETE` api
  2. Execute SQL to Delete the record in Access table

##Setting up Access##
We need to add 2 Refererences in MS Access VBA for the code examples to work.
  1. Microsoft Scripting 1.0
  2. Microsoft XML V6


