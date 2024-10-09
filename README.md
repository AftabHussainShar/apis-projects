# Project API Documentation

This document provides an overview of the API endpoints for the project, including details for sending OTPs, verifying OTPs, and logging in.

## API Endpoints

### 1. Send OTP

**Endpoint:**  
`POST http://127.0.0.1:8000/api/website/send-otp`

**Description:**  
This endpoint is used to send an OTP (One-Time Password) to the user's email.

**Request Body:**  
- `username` (string): The username of the user.
- `email_or_id` (string): The email address or ID of the user.

**Example Request:**

```http
POST /api/website/send-otp HTTP/1.1
Host: 127.0.0.1:8000
Content-Type: application/x-www-form-urlencoded

username=aftav&email_or_id=a03003132335@gmail.com
```

---

### 2. Verify OTP

**Endpoint:**  
`POST http://127.0.0.1:8000/api/website/verify-otp`

**Description:**  
This endpoint is used to verify the OTP sent to the user's email.

**Request Body:**  
- `email_or_id` (string): The email address or ID of the user.
- `otp` (string): The OTP received by the user.
- `password` (string): The user's password.

**Example Request:**

```http
POST /api/website/verify-otp HTTP/1.1
Host: 127.0.0.1:8000
Content-Type: application/x-www-form-urlencoded

email_or_id=a03003132335@gmail.com&otp=337902&password=123
```

---

### 3. Login

**Endpoint:**  
`POST http://127.0.0.1:8000/api/website/login`

**Description:**  
This endpoint is used to log in a user.

**Request Body:**  
- `email_or_id` (string): The email address or ID of the user.
- `password` (string): The user's password.

**Example Request:**

```http
POST /api/website/login HTTP/1.1
Host: 127.0.0.1:8000
Content-Type: application/x-www-form-urlencoded

email_or_id=a03003132335@gmail.com&password=123
```

---
