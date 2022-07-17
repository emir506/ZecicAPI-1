# ZecicAPI-1
Simple RESTfull API

Add new item (e.g. with Postman):
POST /todoitems

Body (RAW/JSON):

{
  "name":"walk dog",
  "isComplete":true
}



Others:

GET /	Browser test, "Hello World"	None	Hello World!
GET /todoitems	Get all to-do items	None	Array of to-do items
GET /todoitems/complete	Get completed to-do items	None	Array of to-do items
GET /todoitems/{id}	Get an item by ID	None	To-do item

PUT /todoitems/{id}	Update an existing item  	To-do item	None
DELETE /todoitems/{id}    	Delete an item    	None	None
