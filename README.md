
# Auth Node.js Mongo Sample

This project is a sample application built with Node.js and MongoDB, demonstrating a simple authentication system. It provides a foundation for creating authentication services using JWT (JSON Web Tokens) with secure routes.

## Features

- User registration with password hashing
- User login with JWT-based authentication
- MongoDB integration for storing user data
- Basic middleware for verifying JWTs

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/AmirDanesh/auth-nodejs-mongo-sample.git
   ```

2. Navigate to the project directory:
   ```bash
   cd auth-nodejs-mongo-sample
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Set up your MongoDB database and add your connection string to the `.env` file:
   ```bash
   MONGO_URI=mongodb://localhost:27017/your_database
   JWT_SECRET=your_jwt_secret
   ```

5. Run the application:
   ```bash
   npm start
   ```

## API Endpoints

### POST /register

Registers a new user.

- **Request Body**:
  ```json
  {
    "username": "user1",
    "password": "password123"
  }
  ```

### POST /login

Logs in a user and returns a JWT.

- **Request Body**:
  ```json
  {
    "username": "user1",
    "password": "password123"
  }
  ```

### GET /profile

Fetches the profile of the currently authenticated user.

- **Authorization**: Bearer token in the request header.

## Technologies Used

- Node.js
- Express
- MongoDB
- JWT Authentication

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
