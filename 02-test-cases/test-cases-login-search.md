# Test Cases – Login & Search Flow (MercadoLibre)

Below are 15 detailed manual test cases designed to validate the login and product search functionality on MercadoLibre’s website.

---

## TC-01 – Login with valid credentials
**Precondition:** User account exists  
**Steps:**  
1. Open the login page  
2. Enter a valid email  
3. Enter a valid password  
4. Click “Login”  
**Expected Result:** User successfully logs in and is redirected to homepage

---

## TC-02 – Login with invalid password
**Steps:**  
1. Enter a valid email  
2. Enter an incorrect password  
3. Click “Login”  
**Expected Result:** Error message “Incorrect password” appears

---

## TC-03 – Login with empty fields
**Steps:**  
1. Click “Login” without entering any information  
**Expected Result:** Validation message “Required field”

---

## TC-04 – Forgot password redirection
**Steps:**  
1. Click “Forgot Password”  
**Expected Result:** User is redirected to the password recovery page

---

## TC-05 – Search for a valid product ("iPhone 15")
**Steps:**  
1. Use the search bar and type “iPhone 15”  
2. Click search  
**Expected Result:** A list of iPhone 15 products appears

---

## TC-06 – Search with empty input
**Steps:**  
1. Click search with an empty field  
**Expected Result:** System displays “Please enter a search term”

---

## TC-07 – Search using special characters
**Steps:**  
1. Enter “!@#$%” in the search bar  
2. Click search  
**Expected Result:** System shows “No results found”

---

## TC-08 – Open product details page
**Precondition:** Search results are displayed  
**Steps:**  
1. Click any product from the results  
**Expected Result:** Product page loads with title, images, and price

---

## TC-09 – Add product to favorites
**Steps:**  
1. Open a product page  
2. Click the “Add to Favorites” icon  
**Expected Result:** Product appears in the user’s favorites list

---

## TC-10 – Apply search filters
**Steps:**  
1. Search for “Samsung phone”  
2. Apply filters (Brand, Condition, Price)  
**Expected Result:** Filtered results update correctly

---

## TC-11 – Validate broken image behavior
**Steps:**  
1. Inspect product images  
**Expected Result:** Placeholder image or alt text displays if image fails to load

---

## TC-12 – Pagination to next page
**Steps:**  
1. Search any product  
2. Click “Page 2”  
**Expected Result:** New set of products loads

---

## TC-13 – Logout functionality
**Precondition:** User is logged in  
**Steps:**  
1. Click “My Account”  
2. Click “Logout”  
**Expected Result:** User session ends; redirected to homepage

---

## TC-14 – Remember Me functionality
**Steps:**  
1. Enter valid login credentials  
2. Select “Remember Me” checkbox  
3. Log in and refresh the page  
**Expected Result:** User stays logged in

---

## TC-15 – Login attempt limit (Security)
**Steps:**  
1. Enter wrong password 5 times  
**Expected Result:** Account temporarily locked or captcha challenge appears

---

