# Title: GET /pet/findByStatus returns 200 OK for invalid status value
***Link to [Jira](https://igor2012lww.atlassian.net/browse/SWAG-13?atlOrigin=eyJpIjoiMTQ5ZjM2OTExM2ZhNDA3OGI3M2VmMThlMWFmZTZlNzciLCJwIjoiaiJ9)***

## Environment: Windows 10 PRO;  Postman  v11.77.2; API Documentation & Design Tools for Teams | Swagger

## Related Test Case: [TCN_03](../../SwaggerPetstore_Testing/Test_Cases/Negative/TCN_03_unavailable_status_query.md)

----

## Preconditions: 

- Api is running. 
- Preconditions are the same as in test-case [TCN_03](../../SwaggerPetstore_Testing/Test_Cases/Negative/TCN_03_unavailable_status_query.md)

## Steps to Reproduce: 

1. Prepare a GET request to /pet/findByStatus.

2. Set query parameter("x-www-form-urlencoded"):

- Key: status
- Value: reserve

3. Execute the request and observe the response.

----

## Actual Result: Response code: 200 OK. Response body is empty.

## Expected Result: Response code: 400 ‘Invalid status value’

----

- Severity: Medium

- Priority: Medium

----

## Screenshot: 

<img src="../../../SwaggerPetstore_Testing/images/bugs/3_find_a_pet_by_unavailable_status.png" alt="" width="70%">
