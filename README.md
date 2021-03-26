# Todo API

**Nazmie -**

**Instructions to run the API tests:**
1. Create a fork of this repository into your own github account.
2. Make a clone of the repo to your Visual Studio IDE on your local machine.
3. Build the solution in your Visual Studio IDE.
4. Select Todo.API indicated below and click the green Play button.  

 ![image](https://user-images.githubusercontent.com/39741659/112698036-7b99a100-8e91-11eb-9808-5e8a58a7103f.png)
 
 5. The API should launch in Swagger:
 
 ![image](https://user-images.githubusercontent.com/39741659/112698123-b0a5f380-8e91-11eb-98d0-c7bdc297f408.png)
 
 6. Launch Google Postman.
 7. Import the following collection into Google Postman:  **Todo API.postman_collection.json**.
 8. Run the DeleteTo operation to remove the last ToDo item created.

Example:

![image](https://user-images.githubusercontent.com/39741659/112699298-31fe8580-8e94-11eb-924d-e500f7c3f5c0.png)


 10. Increment the ID value in each of the following operations before running the tests:  **UpdateIsComplete (all), UpdateToDo, DeleteToDo**

Example:

![image](https://user-images.githubusercontent.com/39741659/112699155-e055fb00-8e93-11eb-93ab-3f0f19ad2257.png)

 11. Click on the main folder of the collection (ToDo API) and click **Run**:
 
 ![image](https://user-images.githubusercontent.com/39741659/112698628-bb14bd00-8e92-11eb-9bff-1a741f0c9177.png)
 
 11. Click **Run Todo API**.

![image](https://user-images.githubusercontent.com/39741659/112699016-9cfb8c80-8e93-11eb-9e73-e460db839b7c.png)

 
 
 **Note:**  Last run test results of the API can be found here:  https://github.com/nazmieh/todo-api/tree/develop/Todo.API/ToDo%20API%20TestResults 
 ---
 

## Overview
This is a simple API providing todo list functionality, stored in a sqlite database. The API is secured using JWT Authentication & role-based authorization. 

* The API is build using dotnet core 3.1
* The API does not work correctly "out of the box"; review app configs before running
* The repo contains a postman collection which demonstrates use of all the API endpoints

## Roles

* **Admin**
  * Can list all users
  * Can view details of a specific user
  * Users cannot be assigned the Admin role via the API
* **User**
  * This is the default User created by the API
  * Can create, edit, list & remove their own todo items
  * Can mark todos they own as complete or incomplete
  * Users cannot see other users todo items

## Notes
There is no setup required, the database will be created when the API is run & the databases will be seeded with the 2 roles & 1 admin user (_admin@test.com_, _test123_).

The API is documented with Swagger, which is implemented with Swashbuckle. Once the app is running, nagivate to [http://localhost:5000/swagger](http://localhost:5000/swagger/index.html) to view the specification for the API.

There is also a Postman collection available in the root of the repository, import the collection to explore the API with Postman if you prefer.

_Please note:_ the unit tests are currently incomplete.

## Instructions
* Create a fork of this repository in your own github account
* If you have any trouble or queries please reach out to us using any of the emails in this README
Depending on the role being assessed instructions may vary.

## QA Automation
Looking at the User role requirements, create at least 3 BDD test scenarios.
### API
* Use the postman collection provided to:
  * Register a user using your name
### Admin
* Can list all users
* Can view details of a specific user
* Users cannot be assigned the Admin role via the API
### User
* This is the default User created by the API
* Can create, edit, list & remove their own todo items
* Can mark todos they own as complete or incomplete
* Users cannot see other users todo items
* Once complete, please send a link to your repository to jehan@geminisolution.co.za or elrika@geminisolution.co.za

