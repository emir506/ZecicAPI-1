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

GET /      (Hello World)

GET /todoitems	

GET /todoitems/{id}

GET /todoitems/complete

PUT /todoitems/{id}	

DELETE /todoitems/{id}    
