# Test Case ID: TCP_01

## Title: Add a new pet to the store using the ‘POST: add a new pet’ function and entering valid data to all the fields. Check the data in the response body.

***Link to [Jira](https://igor2012lww.atlassian.net/browse/SWAG-2?atlOrigin=eyJpIjoiZGM3NDEyZDViMGNhNDI2OTk3NmRiMDkyZjFjZTcwNDEiLCJwIjoiaiJ9)***

----
- Type of testing: Functional
- Test Object: API
- Test Type: Positive
----

## Preconditions:

1. Postman is installed on computer. 

2. Create an environment with variable "swagger" and put in a link "https://petstore.swagger.io/v2".

3. Create a "pet" folder in Collections.

4. "https://petstore.swagger.io/" is available and opened to check documentation.

## Steps:

1. Add a new request to "Pet" folder.

2. Name it "Add new pet to the store" 

3. Change method to "POST"

4. Print to URL-field variable {{swager}} and add /pet in the end. 

5. Open body, chose "raw" and paste an object:
```
{
  "id": 68484,
  "category": {
    "id": 2,
    "name": "Dogs"
  },
  "name": "Jack",
  "photoUrls": [
    "https://lh3.googleusercontent.com/proxy/B37w7N_EbmxPpHubwbDCOI62F1lGRCL3B0kCclMDk0kGu919Z992c_uggBV_VM6_PlGeur1wr92xWA_0XbzYyKSAYS9VXZlULS94pd9FXK-bPfKgtyuP3Q"],
 "tags": [
    {
      "id": 5,
      "name": "Tag-5"
    }
  ],
  "status": "available"
}
```

6. Press the button "Send" observe a response body and status code.

## Expected Result:
- Code 200 ‘Successful operation’
- The entered data and the data in the response body coincide.

## Actual Result:

- Code 200 ‘Successful operation’
- The entered data and the data in the response body coincide.


## Status: Pass
----
## Screenshot: 
<img src="../../../SwaggerPetstore_Testing/images/pet/1_create_a_ pet.png" alt="1_create_a_ pet.png" width="70%">
