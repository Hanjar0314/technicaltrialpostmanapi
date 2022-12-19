# technicaltrialpostmanapi

Postman automated test for the API

1.	Create a Collection with a name “Postman Automated Tes for the API”

2.	Create POST request and save baseurl for Postman Automated Tes for the API Collection. 

3.	According to the API document, properly set Authorization. 
 
4.	POST /numberprettify/:enterNumber

In Post request page, select {{baseurl}} for this project and enter number end points as well as Path Variable (assume there is available for Path Variables in API document). And enter enterNumber path variables.

5.	Enter POST request body in JSON format. 

6.	Write a Test Script for Test. 

      Via Test Scripts in below, I can directly check Test success or not by Response TestResults. Status code can be change to 400 or simiiar for system error or other relevant errors.
  
            pm.test("Status code is 200", function () {
              pm.response.to.have.status(200);
          });

      And by Below Scripts, I can check Test Result Status on Console.

            const response=pm.response.json();
            console.log(response.status);

7.	After completing all above steps, we can able to see API test result.
        1.	For 200 OK, there will be 200 OK status response and corresponding successfully prettified JSON format at body which includes prettified number and other relevant information. Also able to see “OK” in Console as well.
        2.	For 400, incorrect or out of ranged numbers, there will be 400 status response and corresponding error at body in JSON format.
