# Table Structure #
Disucssion on how to configure Local MS Access Tables, where data will be stored locally for offline viewing

It is not compulsory to have your data stored locally. But it is the best approch, if you want to make use of this data in Search, Reports, etc. Check out below, for cases where you need not store your data locally in MS Access tables.


## Primary Key ##
Every time, we create a new record in Firebase (Using `POST` HTTP Request), Firebase automatically generates a Unique 20 Digits String.
We shall be using this as primary key for all the tables. This shall also be the key if we want to link the two tables in a relationship.

## Relationship Between Tables ##
Do not enforse relationship when creating relationships in Access. 
Keep Relationships Simple. Only use One to Many.

*Reason for not Enforcing* : We will be deleting data from server on one client, and then updating the same on another. Hence if that time, if the relationship stops the deletion, it can lead to non consistent data in Acces and Firebase.

## Data Types ##



##Cases where you need not to store data localy.##
  1. Login Logs
  2. Audit Logs
