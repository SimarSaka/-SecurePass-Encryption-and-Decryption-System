## Introduction
The project aims to show how user credentials can be securely handled by encrypting passwords before storing them in a database and verifying those credentials during login. It also focuses on ensuring that each user has a unique identity by checking for duplicate user IDs during the signup process.

Another objective of the project is to follow a **layered and structured approach**, separating the frontend interface, backend logic, and data storage. This helps in understanding real-world application design while keeping the implementation simple and suitable for learning purposes.

Overall, the project aims to provide practical exposure to authentication concepts, database interaction, and secure coding practices at a foundational level.

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/MindMap.png?raw=true)

---

## 1) Digital Entryway (Login vs Signup)
The system starts with two clear options.  
Existing users can log in, while new users can create an account using signup.

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig01.jpeg?raw=true)

---

## 2) Signup Flow (Creating a New Account)
During signup, the system:
1. takes User ID and password  
2. checks if the ID already exists  
3. encrypts the password  
4. stores the record in the database

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig02.jpeg?raw=true)

---

## 3) Checking Uniqueness & Saving Data
The backend uses functions like:
- `userExists()` to check whether an ID is already taken  
- `insertUser()` to save the user safely into MySQL  

Prepared statements are used to make database access safer.

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig03.jpeg?raw=true)

---

## 4) Password Protection (Security Vault)
Before storing a password, the system converts it into an encrypted form using a Caesar Cipher shift.  
This ensures the database does not store the password in plain text.

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig04.jpeg?raw=true)

---

## 5) Caesar Cipher Logic in C++
The Caesar cipher shifts letters and digits by a fixed number.  
The code encrypts each character one-by-one and builds a new encrypted string.

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig05.jpeg?raw=true)

---

## 6) Login Flow (Credential Verification)
During login, the system:
1. receives user ID + password  
2. fetches encrypted password from the database  
3. decrypts it  
4. compares with input password  
5. shows login success or error message

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig06.jpeg?raw=true)

---

## 7) Fetching Stored Password from Database
A specific MySQL query retrieves only the required password field for the given user ID.  
This improves clarity and keeps DB access minimal.

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig07.jpeg?raw=true)

---

## 8) Complete Architecture (UI → Backend → DB)
This diagram shows the overall system layers:
- UI (HTML/CSS)
- Backend logic (C++)
- Encryption and authentication functions
- Database storage (MySQL)

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig08.jpeg?raw=true)

---

## 9) Core Principles of the Project
This project follows basic good practices:
- Layered design (UI + Logic + DB)
- Purposeful function structure
- Basic security focus (prepared statements + encrypted storage)

 ![image alt](https://github.com/SimarSaka/-SecurePass-Encryption-and-Decryption-System/blob/main/Fig09.jpeg?raw=true)

---
