# API Testing – JSONPlaceholder (Postman)

This document contains API tests performed using the public JSONPlaceholder API for QA practice.

---

## Test 1 – GET /users
**Method:** GET  
**Endpoint:** https://jsonplaceholder.typicode.com/users  
**Expected Result:**  
- Status code: 200 OK  
- Response body contains a list of users  
- Fields include: id, name, username, email  

---

## Test 2 – GET /posts
**Method:** GET  
**Endpoint:** https://jsonplaceholder.typicode.com/posts  
**Expected Result:**  
- Status code: 200 OK  
- Response time < 500 ms  

---

## Test 3 – GET /posts/1
**Method:** GET  
**Endpoint:** https://jsonplaceholder.typicode.com/posts/1  
**Expected Result:**  
- Status code: 200  
- userId = 1  
- id = 1  

---

## Test 4 – POST /posts
**Method:** POST  
**Endpoint:** https://jsonplaceholder.typicode.com/posts  
**Body:**
{
  "title": "QA Test",
  "body": "Portfolio test submission",
  "userId": 1
}

**Expected Result:**  
- Status code: 201 Created  
- Response contains the same fields  

---

## Test 5 – DELETE /posts/1
**Method:** DELETE  
**Endpoint:** https://jsonplaceholder.typicode.com/posts/1  
**Expected Result:**  
- Status code: 200 OK  
