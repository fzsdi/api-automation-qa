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
![image](https://user-images.githubusercontent.com/40931282/200143845-06e96f29-26a5-4926-8205-3593b0cb7c29.png)
