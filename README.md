# Description
This is a Node.js backend project that uses MongoDB as the database and JSON Web Tokens (JWT) for secure communication between the backend and frontend. It provides a RESTful API for user authentication, including signup, login, and token-based authorization. JWT tokens are generated upon successful login and are required for accessing protected routes. MongoDB is used to store user data and other application-specific information.

## Features
- **User Authentication**: Secure signup and login using hashed passwords.
- **Token-Based Authorization**: JWT tokens are generated on login and used to authenticate requests to protected routes.
- **RESTful API**: Endpoints for user actions and other app functionalities.
- **MongoDB Integration**: A NoSQL database for efficient data storage and retrieval.

# Requirements

### ExpressJS
ExpressJS is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications. https://expressjs.com

## Mongoose
Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB. https://mongoosejs.com/docs/index.html

## Bcrypt
Bcrypt is a library to help you hash passwords. It uses a password-hashing function that is based on the Blowfish cipher. We will use this to hash sensitive things like passwords.

## Cookie-parser
Cookie-parser is a middleware used to parse the Cookie header and populate req.cookies with an object keyed by the cookie names. Optionally you may enable signed cookie support by passing a secret string, which assigns req.secret so it may be used by other middleware.

##Dotenv
Dotenv is a zero-dependency module that loads environment variables from a .env file into process.env.

## Cors
CORS is a node.js package for providing a Connect/Express middleware that can be used to enable CORS with various options. We don’t necessarily need this as we are developing just the API, however, good that you know in case you want to implement one.

## Express-Validator
Express-Validator is a set of express.js middlewares that wraps validator.js validator and sanitiser functions. You may want to check for an empty request body or validate or even sanitize the request body. This package is very useful for that. You will add one or two of its functions in your code later.

## Nodemon
Nodemon is a tool that helps develop Node.js based applications by automatically restarting the node application when file changes in the directory are detected. With this, you don’t have to manually restart your application each time you make changes. Another powerful tool used mostly in production is pm2. You can check it out pm2.

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
