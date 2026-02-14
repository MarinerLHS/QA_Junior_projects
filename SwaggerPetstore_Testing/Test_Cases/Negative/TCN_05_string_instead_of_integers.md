# Test Case ID: TCN_05

## Title: Create a pet using strings instead of integers.

***Link to [Jira](https://igor2012lww.atlassian.net/browse/SWAG-12?atlOrigin=eyJpIjoiMDM5MTY5NWUwODJiNDBjZTkwZDA5YmE4NzhmNjM3OTEiLCJwIjoiaiJ9)*** 

----

- Type of testing: Functional
- Test Object: API
- Test Type: Negative

----

## Preconditions:

1. Postman is installed on computer. 
2. Create an environment with variable "swagger" and put in a link "https://petstore.swagger.io/v2".
3. Create a "Negative testing" folder in Collections.
4. "https://petstore.swagger.io/" is available and opened to check documentation.

## Steps:

1. Add a new request to "Negative testing" folder.
2. Name the request “Create a pet with string instead of integer”.
3. Change method to "POST"
4. Print to URL-field variable {{swager}} and add /pet. 
5. Open the Body tab.
6. In the "raw" section, set the following json body:
```json
{
  "id": 12,
  "category": {
    "id": "Dogs",
    "name": "string"
  },
  "name": "doggie",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "string"
    }
  ],
  "status": "available"
}
```
(category id string instead of integer)

7. Press the button "Send" observe a response body and status code.

----

## Expected Result:

Code 405 ‘Invalid iput’

## Actual Result:

Code 500 'The server has encountered a situation it does not know how to handle'
```json
{
    "code": 500,
    "type": "unknown",
    "message": "something bad happened"
}
```
----

## Status: Failed 

----

## Screenshot: 

<img src="../../../SwaggerPetstore_Testing/images/negative/5_create_a_pet_with_a_string_instead_of_integer.png" alt="5_create_a_pet_with_a_string_instead_of_integer.png" width="70%">


