# Description
This is a Node.js backend project that uses MongoDB as the database and JSON Web Tokens (JWT) for secure communication between the backend and frontend. It provides a RESTful API for user authentication, including signup, login, and token-based authorization. JWT tokens are generated upon successful login and are required for accessing protected routes. MongoDB is used to store user data and other application-specific information.

## Features
- **User Authentication**: Secure signup and login using hashed passwords.
- **Token-Based Authorization**: JWT tokens are generated on login and used to authenticate requests to protected routes.
- **RESTful API**: Endpoints for user actions and other app functionalities.
- **MongoDB Integration**: A NoSQL database for efficient data storage and retrieval.

# Instructions

## Clone project

## 1 - Install dependencies

## 2 -Edit .env file

#### URI:
##### To get the URI create a cluster on mongodb and connect to database URI
##### Example : URI="mongodb+srv://"username":"password"@node-express-cluster.g5ydx.mongodb.net/?retryWrites=true&w=majority&appName=node-express-cluster"

#### PORT:
##### Example : 5005

#### SECRECT ACESS TOKEN:
##### Type node in your terminal, press the return key,
##### Example: Type crypto.randomBytes(20).toString(‘hex’)

## 3 - Run application using nodemon
##### Example: npm run dev

# Routes

## create a new user:
Post request to localhost:5005/app/auth/register

{
  "first_name: "john",
  "last_name: "doe",
  "email": "john@test.com",
  "password": 12345678
}

## login user:
Post request to localhost:5005/app/auth/login

{
  "email": "john@test.com",
  "password": 12345678
}

## A user can register as admin, to do that edit the MongoDB database and change the role field to 0x88
role: "0x88"

### To test this functionality log in with a valid user with admin access:
Get request to localhost:5005/app/admin

# References:

https://dev.to/m_josh/build-a-jwt-login-and-logout-system-using-expressjs-nodejs-hd2

https://expressjs.com/

https://www.mongodb.com/pt-br/docs/

https://jwt.io/introduction
