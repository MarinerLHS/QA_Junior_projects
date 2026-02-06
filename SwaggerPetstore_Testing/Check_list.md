# Public API SwaggerPetsore testing

### Description : Testing of public API http://Swagger.io  pet store. Using Postman for API requests, 

### Environment : 
- Windows 10 PRO;
- Postman  v11.77.2,
- Jira (link to [Jira](https://igor2012lww.atlassian.net/jira/software/projects/SWAG/boards/68?selectedIssue=SWAG-1))
- http://Swagger.io ,

### Created by : Igor Protsenko

### Status: Done

### Version : 1.1.5

----

**Positive Testing** 

| ID    | Test Description                                                                 | Server response, expected result                                         | Status |
|-------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|:------:|
| TC_1  | Add a new pet to the store using the ‘POST: add a new pet’ function and entering valid data to all the fields. Check the data in the response body. | Application installs and reinstalls successfully without issues                | Pass |
| TC_2  | Find a pet by using a GET request with valid pet ID, which you used when creating a new pet. | Code 200 ‘Successful operation’ The entered data and the data in the response body coincide. | Pass |
| TC_3  | Update a pet using method PUT, add new ‘category’ ID and category name. | Code 200 ‘Successful operation’               | Pass |
| TC_4  | Update a pet in the store with form data using POST method.  | Code 200 ‘Successful operation’ | Pass |
| TC_5  | Upload an image for existing pet, using method POST | Code 200 ‘Successful operation’          | Pass |
| TC_6  | Delete a pet using method DELETE | Code 200 ‘Successful operation’                | Pass |

----

**Negative Testing**

| ID    | Test Description                                                                 | Server response, expected result                                         | Status |
|-------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|:------:|
| TC_1  | Add a new pet to the store entering invalid data to one of / several / all the fields. | Code 405 ‘Invalid input’ The entered data isn’t accepted.           | Pass |
| TC_2  | Find a pet using GET request, with invalid data such as ID.              | Code 400 ‘Invalid ID supplied’ or code 404 ‘Pet not found’             | Pass |
| TC_3  |Find a pet by unavailable ‘status’ using method GET.             | Code 400 ‘Invalid status value’             | Pass |
| TC_4  |Update a pet with form data using wrong format of name and unavailable status              | Code 405 ‘invalid input’            | Pass |
| TC_5  | Create a pet using integers instead of strings.                | Code 405 ‘Invalid input’              | Pass |
| TC_6  | Create a pet with already existing ID     | Code 404             | Pass |

----

**Flow Testing** 


| ID    | Test Description                                                                 | Server response, expected result                                         | Status |
|-------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|:------:|
| TC_1  | Create a pet with new ID, find a pet by ID, delete a pet by method DELETE, try to find deleted pet.      | Code 404 ‘Not Found’             | Pass |
| TC_2  | Place an order for a pet, find an order using method GET, delete an order, try to find deleted order.    | Code 404 ‘Not Found’             | Pass |
| TC_3  | Create user, log created user into the system. Update users email and password using method PUT. Try to log user with old credentials  | Code 400 ‘Invalid username/password supplied’            | Pass |



