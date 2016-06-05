
### Build and run

#### Configurations

Open the `application.properties` file and set your own configurations.

#### Prerequisites

- Java 8
- Maven > 3.0
- MySQL 5

#### From terminal

Go on the project's root folder, then type:

    $ mvn spring-boot:run


### RESTFul Operations 
RESTful to add a contact to the app: 
POST http://localhost:8080/contacts/
```
    {
  		"id": 7,
  		"name": "name23213",
  		"email": "email3213",
  		"profession": "profession323"
	}
```

RESTful to delete a contact to the app: 
DELETE http://localhost:8080/contacts/[id]
```
Contact successfully deleted!
```

RESTful to list the contacts (Should have sorting and pagination support):

GET http://localhost:8080/contacts/list
GET http://localhost:8080/contacts/list?page=0&size=2
GET http://localhost:8080/contacts/list?page=0&size=2&

```
	[
	  {
	    "id": 3,
	    "name": "name",
	    "email": "email",
	    "profession": "profession"
	  },
	  {
	    "id": 4,
	    "name": "name",
	    "email": "email",
	    "profession": "profession"
	  },
	  {
	    "id": 5,
	    "name": "name",
	    "email": "email",
	    "profession": "profession"
	  }
	]
```
   
RESTful to update a contact:
PUT http://localhost:8080/contacts/5
```
	{
  		"id": 5,
  		"name": "pancho villa 23456789",
  		"email": "rosama7777@gmail.com",
  		"profession": "employee"
	}
```

RESTful to search for recent 5 contacts who are unemployed (Should have sorting and pagination support)

GET http://localhost:8080/contacts/list-unemployee
```
	[
  		{
	    "id": 4,
	    "name": "mauro gomez",
	    "email": "rosama77@gmail.com",
	    "profession": "unemployee"
	  },
	  {
	    "id": 3,
	    "name": "pancho villa",
	    "email": "rosama7777@gmail.com",
	    "profession": "unemployee"
	  }
	]
```
