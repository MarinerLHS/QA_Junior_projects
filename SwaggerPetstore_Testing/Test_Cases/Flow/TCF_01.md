# Test Case ID: TCF_01

## Title: Create a pet with new ID, find a pet by ID, delete a pet by method DELETE, try to find deleted pet.


----

- Type of testing: Functional

- Test Object: API

- Test Type: Positive/Negative

----

## Preconditions:

1. Postman is installed on computer. 
2. Create an environment with variable "swagger" and put in a link "https://petstore.swagger.io/v2".
3. "https://petstore.swagger.io/" is available and opened to check documentation.
4. Create a new Collection and name it "Flow test.

## Steps:

**1. Add a 4 new requests to "Flow test" folder.**
**2. Name the requests:**
- "01 Create a pet" (method POST) URL: {{swagger}}/pet
- "02 Get pet by ID" (method GET) URL: {{swagger}}/pet/{{pet_id}}
- "03 Delete a pet" (method DELETE) URL: {{swagger}}/pet/{{pet_id}}
- "04 Get deleted pet" (method GET) URL: {{swagger}}/pet/{{pet_id}}
**3. Filling requests with data:**
  ----
  - "01 Create a pet":

    1.Add to body/RAW following JSON data: 
 
  ```json
  {
  "id": {{$randomInt}},
  "category": {
    "id": 2,
    "name": "Dogs"
  },
  "name": "Jack",
  "photoUrls": [
    ""
  ],
  "tags": [
    {
      "id": 5,
      "name": "Tag-1"
    }
  ],
  "status": "available"
}
```
2. Add following code to Scripts/Post-respone: 
                        
```javascript
console.log("test script for POST method")
pm.collectionVariables.set("pet_id", pm.response.json().id)

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Content-Type is present", function () {
    pm.response.to.have.header("Content-Type");
});

pm.test("Response time is less than 9000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(9000);
});

pm.test("Response body contains category id", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.category.id).to.equal(2);
});

pm.test("Response body contains name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.name).to.equal("Jack");
});

pm.test("Response body contains category name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.category.name).to.equal("Dogs");
}); 
```
3. Save the request

----

- "02 Get pet by ID":

   1.Add following script to Scripts/Post-response: 

```javascript
console.log("test script for POST method")
pm.collectionVariables.set("pet_id", pm.response.json().id)

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Content-Type is present", function () {
    pm.response.to.have.header("Content-Type");
});

pm.test("Response time is less than 9000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(9000);
});

pm.test("Response body contains category id", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.category.id).to.equal(2);
});

pm.test("Response body contains name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.name).to.equal("Jack");
});

pm.test("Response body contains category name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.category.name).to.equal("Dogs");
});
```
2. Save the request.

----

- "03 Delete a pet"

   1.Add following script to Scripts/Post-response: 

   ```javascript
  pm.test("Status code is 200", function () {
    pm.response.to.have.status(200); 
});```

2. Save the request 

----

- "04 Get deleted pet":

   1.Add following script to Scripts/Post-response:
  
  ```javascript
  pm.test("Status code is 404", function () {
    pm.response.to.have.status(404); 
});```

2. Save the request.

----

4. Run the collection add 100ms delay between requests.
5. Observe the response and status of tests. 

----

## Expected Result:
All tests are passed, the code responses from server are as expected to documentation. 

## Actual Result:

Test executed successfully.

----

## Status: Pass

----

## Screenshot: 

[Folder with screenshots]()
