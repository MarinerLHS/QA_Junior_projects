# Title: POST method for updating a pet with unavailable status returns code 200.
***Link to [Jira](https://igor2012lww.atlassian.net/browse/SWAG-14?atlOrigin=eyJpIjoiZmY2OTQ5YjVmZTJiNDNlNzhiMWVhZDNjYmZmZjM2NTYiLCJwIjoiaiJ9)***

## Environment: Windows 10 PRO;  Postman  v11.77.2; API Documentation & Design Tools for Teams | Swagger

## Related Test Case: [TCN_04](../../SwaggerPetstore_Testing/Test_Cases/Negative/TCN_04_update_a_pet_with_wrong_parameters.md)

----

## Preconditions: 

- Api is running. 
- Preconditions are the same as in test-case [TCN_04](../../SwaggerPetstore_Testing/Test_Cases/Negative/TCN_04_update_a_pet_with_wrong_parameters.md)

## Steps to Reproduce: 

1. Prepare a POST request to /pet/68484.

2. In the "x-www-form-urlencoded" section, set the following parameters:

- Key: name, Value: '"L@cky'"
- Key: status, Value: reserve

3. Execute the request and observe the response.

----

## Actual Result:  
- Code 200 'Request successful'
```
{
    "code": 200,
    "type": "unknown",
    "message": "68484"
}
```

- The pet is created with unavailable status.
- Subsequently, GET /pet/findByStatus?status=reserve returns this pet.

## Expected Result: Response code: 400 ‘Invalid status value’

----

- Severity: High

- Priority: Medium

----

## Screenshot: 

<img src="../../../" alt="" width="70%">
