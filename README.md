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

### Create###
  1. Use `beforeUpdate` event on the Access Form to Hit `POST` api.
  2. Get Unique ID in response and set this as the `Record Id`
  3. Now Access will save the record
  
### Read###
  1. Create Refresh Button and Hit `GET` api
  2. Get data in Json
  3. Parse this Json and save it in the table
  
### Update###
  1. Use `beforeUpdate` event on the Access Form to Hit `PATCH` api.
  2. Now access will save the record
  
### Delete###
  1. Create Delete Button and Hit `DELETE` api
  2. Execute SQL to Delete the record in Access table

##Setting up Access##
We need to add 2 Refererences in MS Access VBA for the code examples to work.
  1. Microsoft Scripting 1.0
  2. Microsoft XML V6
I am using MS Access 2013 for development and running the code shared here. 99.99% of the code will run in 2010 and 2016 version too. If you are still using 2007, you are taking your chances. 

##Tools Required##
We will require the following classes / modules for fast development. You can create your own, or use other classes which you are comfurtable with.
  1. **Json Parcing** - All response from Firebase is in Json Format. This Module will parse the data and give us Arrays to warok with.
  2. **HTTP Request** - Call firebase API. Used for `POST`, `PATCH`, `DELETE`. Important where want the response to come come back and only then Access will continue processing
  3. **Asyncronous HTTP Request** - Call Firebase API. This improves User Expereince as it will not freeze Access. Access will not wait for the response to come back, processing will continue.


## Let's Get Started##



## Helping this project##
If you are an exprerienced developer or MS Access or Firebase.
  Please ping me on [Twitter] (https://twitter.com/adarshmadrecha) `@adarshmadrecha` or Git Hub. Will add you as contibutor to this project itself. No need for Pull reqests. 
  
# Credits #
  1. [Json Parser]  (http://stackoverflow.com/a/7300926/4050261) -  [Codo] (http://stackoverflow.com/users/413337/codo)
  2. [Asynchronous HTTP Request ] (http://www.utteraccess.com/wiki/index.php/Asynchronous_HTTP_Request_Class) - Rick Cooney
  3. [HTTP Request ] (http://stackoverflow.com/a/158657/4050261) - Bill
