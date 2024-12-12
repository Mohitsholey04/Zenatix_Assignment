# Django Project: User Authentication API

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Database Schema](#database-schema)
4. [API Structure](#api-structure)
5. [Setup Instructions](#setup-instructions)
6. [Code Structure](#code-structure)
7. [Postman Collection](#postman-collection)
8. [Best Practices Followed](#best-practices-followed)
9. [Git Usage](#git-usage)
10. [Comments and Documentation](#comments-and-documentation)

## Project Overview

This project is a Django-based RESTful API for user authentication, leveraging JWT (JSON Web Tokens) for secure authentication. The API supports features such as user registration, login, and protected endpoints requiring authentication.

## Features

- **User Authentication**: Implements login and logout functionality using JWT.
- **Custom User Model**: Extends the default user model for flexibility.
- **Media File Handling**: Supports uploading and managing media files.
- **Database Integration**: Configured for SQLite (development) and PostgreSQL (production).

## Database Schema

The database schema includes:

- **CustomUser**: Custom user model extending `AbstractUser`.
- **Media Files**: Storage and management of user-uploaded files.
- **JWT Tokens**: Managed via Django REST Framework SimpleJWT.

For details, see the `models.py` file in the `myapp` directory.

## API Structure

| Endpoint               | Method | Description                |
|------------------------|--------|----------------------------|
| `/api/register/`       | POST   | Register a new user        |
| `/api/login/`          | POST   | Log in and obtain a token  |
| `/api/token/refresh/`  | POST   | Refresh the JWT token      |
| `/api/protected/`      | GET    | Access a protected resource |

For a complete list of endpoints, refer to the `urls.py` file and the included [Postman Collection](#postman-collection).

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Mohitsholey04/Zenatix_Assignment.git
   cd Zenatix_Assignment
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Apply Migrations**:
   ```bash
   python manage.py migrate
   ```

4. **Run the Development Server**:
   ```bash
   python manage.py runserver
   ```

5. **Access the API**:
   Navigate to `http://127.0.0.1:8000/api/` to interact with the API.

## Code Structure

```
ua/
├── myapp/
│   ├── migrations/
│   ├── models.py
│   ├── serializers.py
│   ├── views.py
│   ├── urls.py
├── ua/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
├── media/
├── manage.py
├── requirements.txt
```

## Postman Collection

A Postman collection for testing the API is included in the repository as `PostmanCollection.json`. Import it into Postman to test the API endpoints.

## Best Practices Followed

1. **Django Framework Components**:
   - Used Django REST Framework for API development.
   - Custom user model with JWT-based authentication.

2. **Code Organization**:
   - Views, serializers, and models are modular and well-documented.
   - `settings.py` is structured for easy production deployment.

3. **Security**:
   - Sensitive data like `SECRET_KEY` and database credentials are managed through environment variables.
   - Implemented CSRF protection and secure token handling.

## Git Usage

- **Source Code Hosted**: [GitHub Repository](https://github.com/Mohitsholey04/Zenatix_Assignment)
- **Branch Management**:
  - `main`: Production-ready code.


## Comments and Documentation

- Code is thoroughly commented for clarity.
- Inline comments explain the purpose of complex logic.
- Function docstrings describe input parameters, processing, and output.

---

Feel free to contribute to this project by submitting issues or pull requests on GitHub!
