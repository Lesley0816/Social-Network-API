# Social-Network-API

This is a social network API built with Node.js, Express, and MongoDB. It allows for the creation, updating, and deletion of users, thoughts, reactions, and friends. This API handles large amounts of unstructured data efficiently using a NoSQL database.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [API Routes](#api-routes)
  - [Users](#users)
  - [Thoughts](#thoughts)
  - [Reactions](#reactions)
  - [Friends](#friends)
- [License](#license)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/social-network-api.git
   cd social-network-api

2. Install dependencies:
   npm install

3. Create a .env file in the root directory and add your MongoDB connection string and port number:
   MONGODB_URI=mongodb://localhost:27017/socialNetworkDB
   PORT=3001

4. Start the server:
   npm run dev

## Usage
Once the server is running, you can interact with the API using tools like Insomnia or Postman.

### Example Requests
- Fetch all users:

GET /api/users


- Create a new user:

POST /api/users
Content-Type: application/json

{
  "username": "johndoe",
  "email": "johndoe@example.com"
}


- Update a user:

PUT /api/users/:userId
Content-Type: application/json

{
  "username": "johnupdated",
  "email": "johnupdated@example.com"
}

- Delete a user: 

DELETE /api/users/:userId

## API Routes

- Users
    GET /api/users: Fetch all users.
    GET /api/users/:userId: Fetch a single user by ID.
    POST /api/users: Create a new user.
    PUT /api/users/:userId: Update a user by ID.
    DELETE /api/users/:userId: Delete a user by ID.
    POST /api/users/:userId/friends/:friendId: Add a friend to a user's friend list.
    DELETE /api/users/:userId/friends/:friendId: Remove a friend from a user's friend list.

- Thoughts
    GET /api/thoughts: Fetch all thoughts.
    GET /api/thoughts/:thoughtId: Fetch a single thought by ID.
    POST /api/thoughts: Create a new thought.
    PUT /api/thoughts/:thoughtId: Update a thought by ID.
    DELETE /api/thoughts/:thoughtId: Delete a thought by ID.

- Reactions
    POST /api/thoughts/:thoughtId/reactions: Add a reaction to a thought.
    DELETE /api/thoughts/:thoughtId/reactions/:reactionId: Remove a reaction from a thought.

- Friends
    POST /api/users/:userId/friends/:friendId: Add a friend to a user's friend list.
    DELETE /api/users/:userId/friends/:friendId: Remove a friend from a user's friend list

## License
This project is licensed under the MIT License. See the LICENSE file for details.


