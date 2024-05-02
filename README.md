# Chat Application

A real-time chat application built with React, Node.js, Express, and MongoDB.

---

## Table of Contents

- [Setup and Run Instructions](#setup-and-run-instructions)
- [API Route Descriptions](#api-route-descriptions)
- [Necessary Environment Configurations](#necessary-environment-configurations)

---

## Setup and Run Instructions

1. Clone the Repository:

   git clone <repository_url>

2. Navigate to the Project Directory:

    cd chat-application

3. Install Dependencies:

    npm install

4. Start the Frontend:

    cd frontend
    npm run start

5. Start the Backend:

    cd backend
    npm run dev
    
6. Access the Application:

   -> Frontend: http://localhost:3000
   -> Backend: http://localhost:8080

## API Route Descriptions

1. Authentication Routes

-> POST /api/auth/signup
    Input: JSON object containing user details (username, email, password)
    Output: Newly created user object with JWT token

-> POST /api/auth/login
    Input: JSON object containing user credentials (email, password)
    Output: User object with JWT token

-> GET /api/auth/logout
    Input: None
    Output: Success message upon logout

2. User Routes

-> GET /api/users
    Input: None
    Output: List of all users

-> GET /api/users/:id
    Input: User ID
    Output: User object for the given ID

-> PUT /api/users/status
    Input: JSON object containing user ID and status (available/busy)
    Output: Success message

3. Message Routes

-> GET /api/messages/:senderId/:receiverId
    Input: Sender ID and Receiver ID
    Output: List of messages between the sender and receiver

-> POST /api/messages/send
    Input: JSON object containing sender ID, receiver ID, and message text
    Output: Success message upon sending the message

## Necessary Environment Configurations

1. Backend Environment Variables:
    1.1 MONGODB_URI: MongoDB connection URI
    1.2 JWT_SECRET: Secret key for JWT token generation

2. Frontend Environment Variables:
    No specific environment variables required for the 
    
3. Additional Configurations:
    3.1 Ensure MongoDB is installed and running
    3.2 Update backend .env file with appropriate MongoDB URI and JWT secret


