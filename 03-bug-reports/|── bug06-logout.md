### BUG-06 – Logout Does Not Clear User Session

**Severity:** Critical  

**Description:**  
After logging out, the user session remains active when returning to the site.

**Steps to Reproduce:**  
1. Log in to MercadoLibre  
2. Click “Logout”  
3. Open the site again  

**Expected Result:**  
User should be logged out.

**Actual Result:**  
User is still logged in.

**Evidence:**  
"Logout failed – session persisted"
