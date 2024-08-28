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
  "password": "pass123"
  }
## Configuration

Add the following settings to your `settings.py` file:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
    'rest_framework_simplejwt',
    ...
]

REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ),
}

from datetime import timedelta

SIMPLE_JWT = {
    'ACCESS_TOKEN_LIFETIME': timedelta(minutes=30),
    'REFRESH_TOKEN_LIFETIME': timedelta(days=1),
    'ROTATE_REFRESH_TOKENS': False,
    'BLACKLIST_AFTER_ROTATION': True,
    'ALGORITHM': 'HS256',
    'SIGNING_KEY': 'your_secret_key_here',
    'AUTH_HEADER_TYPES': ('Bearer',),
}

Response:
{
  "refresh": "your_refresh_token",
}

Django Banking Application with Deposit, Withdraw, and Exit Functionalities

Add the following settings to your `settings.py` file:
INSTALLED_APPS = [
    ...
    'rest_framework',
    'rest_framework_simplejwt',
    'bank',  # Assuming your Django app is named 'bank'
    ...
]

REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ),
}

from datetime import timedelta

SIMPLE_JWT = {
    'ACCESS_TOKEN_LIFETIME': timedelta(minutes=30),
    'REFRESH_TOKEN_LIFETIME': timedelta(days=1),
    'ROTATE_REFRESH_TOKENS': False,
    'BLACKLIST_AFTER_ROTATION': True,
    'ALGORITHM': 'HS256',
    'SIGNING_KEY': 'your_secret_key_here',
    'AUTH_HEADER_TYPES': ('Bearer',),
}

 Django Banking Application with Login, Logout History, and Transaction History
Add the following settings to your `settings.py` file:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
    'rest_framework_simplejwt',
    'bank',  # Assuming your Django app is named 'bank'
    ...
]

REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ),
}

from datetime import timedelta

SIMPLE_JWT = {
    'ACCESS_TOKEN_LIFETIME': timedelta(minutes=30),
    'REFRESH_TOKEN_LIFETIME': timedelta(days=1),
    'ROTATE_REFRESH_TOKENS': False,
    'BLACKLIST_AFTER_ROTATION': True,
    'ALGORITHM': 'HS256',
    'SIGNING_KEY': 'your_secret_key_here',
    'AUTH_HEADER_TYPES': ('Bearer',),
}
This Django-based banking application is designed to provide secure user authentication and basic banking functionalities such as login/logout tracking and transaction history management. The application uses Django REST Framework (DRF) and Simple JWT for authentication, allowing users to interact with the system through RESTful APIs. 


  "access": "your_access_token"
}
