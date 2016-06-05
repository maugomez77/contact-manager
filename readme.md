
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


### Usage

### Use the following urls to invoke controllers methods and see the interactions with the database:

### Add a contact: 
  
    POST http://localhost:8080/contacts/
    ```javascript
    {
  		"id": 7,
  		"name": "name23213",
  		"email": "email3213",
  		"profession": "profession323"
	}
	```

### For the delete method: 
    
    DELETE http://localhost:8080/contacts/[id]
    
	Contact successfully deleted!
	
### List the contacts (Should have sorting and pagination support):
	
	GET http://localhost:8080/contacts/list
	GET http://localhost:8080/contacts/list?page=0&size=2
	GET http://localhost:8080/contacts/list?page=0&size=2&
	```json
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
   
### Update a contact
	PUT http://localhost:8080/contacts/5
	```json
	{
  		"id": 5,
  		"name": "pancho villa 23456789",
  		"email": "rosama7777@gmail.com",
  		"profession": "employee"
	}
	```

### Search recent 5 contacts added who are unemployed (Should have sorting and pagination support)
	GET http://localhost:8080/contacts/list-unemployee
	```json
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
