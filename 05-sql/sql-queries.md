# SQL Queries – MercadoLibre Login & Search Testing (Ana Zoila)

These SQL queries simulate backend validation for the MercadoLibre login, search, favorites, and pagination features.  
They correspond directly to the test cases and bug reports in this QA portfolio.

---

## 🔐 LOGIN MODULE

### 1. Check if a user email exists
```sql
SELECT id, name, email 
FROM users 
WHERE email = 'testuser@mercadolibre.com';
```

### 2. Validate correct password
```sql
SELECT id 
FROM users 
WHERE email = 'testuser@mercadolibre.com'
  AND password = 'CorrectPassword123';
```

### 3. Check failed login attempts (for lockout testing)
```sql
SELECT user_id, failed_attempts 
FROM login_attempts 
WHERE user_id = 1;
```

### 4. Reset failed login attempts (used before regression)
```sql
UPDATE login_attempts
SET failed_attempts = 0
WHERE user_id = 1;
```

---

## 🔍 SEARCH MODULE

### 5. Get products matching search term “iPhone 15”
```sql
SELECT id, title, price 
FROM products 
WHERE title ILIKE '%iphone 15%';
```

### 6. Validate price filter for products
```sql
SELECT * 
FROM products 
WHERE price BETWEEN 500 AND 1500;
```

### 7. Detect missing or broken product images
```sql
SELECT id, title 
FROM products 
WHERE image_url IS NULL
   OR image_url = ''
   OR image_url NOT LIKE 'http%';
```

---

## ⭐ FAVORITES MODULE

### 8. Check if a product was added to favorites
```sql
SELECT user_id, product_id 
FROM favorites 
WHERE user_id = 1;
```

---

## 📄 PAGINATION MODULE

### 9. Validate page 2 (next 20 items)
```sql
SELECT * 
FROM products
ORDER BY id
LIMIT 20 OFFSET 20;
```

---

## 📦 GENERAL VALIDATION

### 10. Count total products in catalog
```sql
SELECT COUNT(*) FROM products;
```

---
