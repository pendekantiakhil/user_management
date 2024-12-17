
# User Management 📋  

## Project Overview  
The **User Management System** is a robust platform for managing user profiles, role assignments, and secure functionalities like password validation and image uploads. This project includes critical bug fixes, enhancements, and comprehensive testing to ensure a seamless user experience.

---
## Project Submissions 🌐  
- **Closed Issues**:  
   - [#18](https://github.com/pendekantiakhil/user_management/issues/18): Error in Image Uploader  
   - [#15](https://github.com/pendekantiakhil/user_management/issues/15): Multiple Email/Nickname Validation  
   - [#12](https://github.com/pendekantiakhil/user_management/issues/12): Password Strength Validation  
   - [#9](https://github.com/pendekantiakhil/user_management/issues/9): Profile Picture URL Validation  
   - [#7](https://github.com/pendekantiakhil/user_management/issues/7): Role Downgrade During Email Verification  
   - [#5](https://github.com/pendekantiakhil/user_management/issues/5): User-ID Missing in Verify Email  
   - [#1](https://github.com/pendekantiakhil/user_management/issues/1): Docker Dependency Fix  

- **DockerHub**: [Docker Image Link Here](https://hub.docker.com/r/vp679/user_management/)  

## Features Implemented  

### 🚀 **Enhanced Profile Picture Upload using MinIO**  
- Implemented image upload functionality with MinIO as the object storage system.  
- Features include:  
   - File format validation (`.jpg`, `.jpeg`, `.png`).  
   - Image resizing for optimization.  
   - Secure storage and retrieval of image URLs.  

---

## Bugs Fixed  

### 🐞 **Error in Image Uploader**  
- **Issue**: Incorrect file handling led to upload failures.  
- **Fix**: Refined file handling logic to ensure successful uploads.  
- **Issue Link**: [#18](https://github.com/pendekantiakhil/user_management/issues/18)  

### 🐞 **Multiple Email and Nicknames Causing Test Failures**  
- **Issue**: Duplicate emails and nicknames caused test case failures.  
- **Fix**: Added database constraints and validation checks to prevent duplicates.  
- **Issue Link**: [#15](https://github.com/pendekantiakhil/user_management/issues/15)  

### 🐞 **Password Strength Not Validated**  
- **Issue**: Weak passwords were accepted during user registration.  
- **Fix**: Enforced strong password validation (uppercase, lowercase, numbers, and special characters).  
- **Issue Link**: [#12](https://github.com/pendekantiakhil/user_management/issues/12)  

### 🐞 **Profile Picture URL Validation Not Done**  
- **Issue**: Invalid profile picture URLs were accepted.  
- **Fix**: Added regex validation to ensure proper URL formats.  
- **Issue Link**: [#9](https://github.com/pendekantiakhil/user_management/issues/9)  

### 🐞 **Prevent Unauthorized Role Downgrade During Email Verification**  
- **Issue**: User roles were downgraded unintentionally during email verification.  
- **Fix**: Ensured roles are preserved during the email verification process.  
- **Issue Link**: [#7](https://github.com/pendekantiakhil/user_management/issues/7)  

### 🐞 **User-ID is None Upon Clicking Verify Email**  
- **Issue**: Verification failed when the user-ID was missing.  
- **Fix**: Fixed the generation and inclusion of valid user-IDs in the verification email.  
- **Issue Link**: [#5](https://github.com/pendekantiakhil/user_management/issues/5)  

### 🐞 **Docker Image Dependencies Issue**  
- **Issue**: Build failures occurred due to dependency conflicts.  
- **Fix**: Updated dependencies and optimized the `Dockerfile`.  
- **Issue Link**: [#1](https://github.com/pendekantiakhil/user_management/issues/1)  

---

## Testing and Quality Assurance 🧪  

- Implemented unit tests to validate:  
   - Duplicate email and nickname validation.  
   - Password strength enforcement.  
   - Profile picture upload and URL validation.  
- Improved test coverage to handle edge cases and ensure reliability.  

---

## Project Setup ⚙️  

1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/pendekantiakhil/user_management.git  
   cd user_management  
   ```  

2. **Run Docker Containers**  
   ```bash  
   docker-compose up --build -d  
   ```  

3. **Run Migrations and Start Server**  
   ```bash  
   alembic upgrade head  
   uvicorn app.main:app --reload  
   ```  

4. **Access the Application**  
   - API Documentation: [http://localhost:8000/docs](http://localhost:8000/docs)  

---

## Final Notes ✨  

This project demonstrates a comprehensive approach to bug resolution, feature enhancement, and rigorous testing to deliver a reliable user management system.  
