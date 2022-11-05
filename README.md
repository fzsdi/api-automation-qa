This is a project to automate some of the test cases for the following API address:<br/> https://newsapi.org/v2/everything

ER stands for expected result and the emoji shown in front of the ER represents the test result (Failed/Passed).

## List of test cases
- **HTTP status code `200`**
  * ER: should return `200 HTTP` status code. ✔️
- **Valid response**
  * ER: should return valid response in `JSON` format after sending `GET` request like it should have body, should be `JSON` data the status param should be equal to **"ok"**. ✔️
- **Body matches string**
  * ER: the response body keys should contain certain strings. ✔️
- **Response time**
  * ER: the response time should be less than 400ms (the API's average response time). ✖️
- **Response `JSON` schema validation**
  * ER: the response body `JSON` should match the defined schema. ✔️
- **Invalid API key**
  * ER: should not return the response and should return a valid error message with `401 (unauthorized) HTTP` status code. ✔️
- **Conditional checking `sortBy`**
  * ER: if `sortBy` is equal to **"publishedAt"**, the articles should be ordered by date and descending. ✔️
- **Check if response body has results**
  * ER: the atricles array should at least have one element. ✔️
- **Check from date in request**
  * ER: if from date is no today and or the days before today no articles should be returned. ✔️
- **Check URL in response**
  * ER: this parameter should be a valid date. ✔️
- **Check returned header**
  * ER: the header should contain `Content-Type`. ✔️
- **Check the order of parameters in request**
  * ER: it should not be order sensitive and should return valid reponse even with an unordered request parameters. ✔️

## In Postman
To run the automated test cases and start testing the API, import `postman_collection.json` in Postman.<br/> Note that before running the collection, go to https://newsapi.org to get a free API key and add it to the `Authorization` tab of the collection in Postman.

<img width="679" alt="image" src="https://user-images.githubusercontent.com/40931282/200144141-410b2b87-e6e3-4ead-8556-db57468ff6a4.png">

After that you can send the request and see the tests results.

<img width="571" alt="image" src="https://user-images.githubusercontent.com/40931282/200144351-4426e4b4-4a96-47ae-ac75-3801de140496.png">
