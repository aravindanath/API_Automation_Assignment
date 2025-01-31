# Automation Assignment

## Technical Test Guidance for Candidate

### Objective
Develop an automated test framework to execute the tasks below using Java and Rest Assured. The framework can be built from scratch or based on existing templates, following any format you prefer. The completed work should be uploaded to a Git repository and shared prior to the interview.

---

## Task 1: API Assignment

This is a REST API automation assignment. Please use any automation tool, preferably **Rest Assured** with any unit testing framework.

### **Steps to Automate:**

#### 1. Add an Item

**Sample Request:**
```sh
curl --location 'https://restful-booker.herokuapp.com/booking' \
--header 'Content-Type: application/json' \
--data '{
    "firstname" : "testFirstName",
    "lastname" : "lastName",
    "totalprice" : 10.11,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2022-01-01",
        "checkout" : "2024-01-01"
    },
    "additionalneeds" : "testAdd"
}'
```

**Expected Response:**
```json
{
    "bookingid": 1416,
    "booking": {
        "firstname": "testFirstName",
        "lastname": "lastName",
        "totalprice": 10,
        "depositpaid": true,
        "bookingdates": {
            "checkin": "2022-01-01",
            "checkout": "2024-01-01"
        },
        "additionalneeds": "testAdd"
    }
}
```

#### 2. Validate the Added Item Using List API

**Request:**
```sh
curl --location 'https://restful-booker.herokuapp.com/booking/1416'
```

**Expected Response:**
```json
{
    "firstname": "testFirstName",
    "lastname": "lastName",
    "totalprice": 10,
    "depositpaid": true,
    "bookingdates": {
        "checkin": "2022-01-01",
        "checkout": "2024-01-01"
    },
    "additionalneeds": "testAdd"
}
```

### **Additional Requirements:**
- **Generate a report** with test results (Pass/Fail).
- **Implement negative test cases** for better coverage.

---

## **Important Points**

- The automation framework should be developed using **Java** as the primary programming language.
- **Rest Assured** should be used for API automation.
- Follow proper **coding standards**.

---

## **Submission Guidelines**
1. Develop the automation framework following the outlined steps.
2. Store the code in a **Git repository**.
3. Share the repository link before the interview.

---

### **References**
- [Rest Assured Documentation](https://rest-assured.io/)
- [Restful Booker API](https://restful-booker.herokuapp.com/)

---

**Note:** This document is marked **Internal**. Do not distribute outside of the organization.
