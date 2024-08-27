# django-project
This project is a basic authentication API built using Django and Django Rest Framework (DRF). It supports user registration, login, and profile management, using JSON Web Tokens (JWT) for secure authentication.

Features:
User Registration: Allows new users to create an account.
User Login: Authenticates users and returns a JWT token for further API access.
User Profile: Retrieves the authenticated user's profile information.

Prerequisites:
Python 3.x
Django 3.x or higher
Django Rest Framework
Django Rest Framework SimpleJWT

Register a new user: POST /api/register/
Request body:
{
  "username": "user1",
  "password": "pass1234",
  "email": "user1@example.com"
}
Login: POST /api/login/

Request body:
{
  "username": "user1",
  "password": "pass1234"
}
Response:
{
  "refresh": "your_refresh_token",
  "access": "your_access_token"
}
