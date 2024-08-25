---

# Voting Application

This is a backend application for a voting system where users can vote for candidates. It provides functionalities for user authentication, candidate management, and voting.

## Features

- User sign up and login with Aadhar Card Number and password
- User can view the list of candidates
- User can vote for a candidate (only once)
- Admin can manage candidates (add, update, delete)
- Admin cannot vote

## Technologies Used

- Node.js
- Express.js
- MongoDB
- JSON Web Tokens (JWT) for authentication

## Live Deployment

The application is live and accessible at: [https://voting-app-e6eq.onrender.com](https://voting-app-e6eq.onrender.com)

## Docker

The project is containerized using Docker. You can pull the Docker image from Docker Hub using the following command:

```bash
docker pull sanketdeshmukh07/voting-app:v1
```

### Running the Docker Container

To run the Docker container locally, use the following command:

```bash
docker run -d -p 3000:3000 --env-file .env --name voting-app-container sanketdeshmukh07/voting-app:v1
```

- `-d`: Run the container in detached mode.
- `-p 3000:3000`: Map port 3000 on your local machine to port 3000 in the container.
- `--env-file .env`: Specify the environment variables from the `.env` file.
- `--name voting-app-container`: Assign a name to the running container.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/SanketDeshmukh007/Voting-App.git
   ```

2. Navigate into the project directory:

   ```bash
   cd Voting-App
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Set up environment variables in a `.env` file based on `.env.example`.

5. Start the application:

   ```bash
   npm start
   ```

## API Endpoints

### Authentication

#### Sign Up
- `POST user/signup`: Sign up a user

#### Login
- `POST user/login`: Login a user

### Candidates

#### Get Candidates
- `GET /candidate`: Get the list of candidates

#### Add Candidate
- `POST /candidate`: Add a new candidate (Admin only)

#### Update Candidate
- `PUT /candidate/:id`: Update a candidate by ID (Admin only)

#### Delete Candidate
- `DELETE /candidate/:id`: Delete a candidate by ID (Admin only)

### Voting

#### Get Vote Count
- `GET /candidate/vote/count`: Get the count of votes for each candidate

#### Vote for Candidate
- `POST /candidate/vote/:id`: Vote for a candidate (User only)

### User Profile

#### Get Profile
- `GET /user/profile`: Get user profile information

#### Change Password
- `PUT /user/profile/password`: Change user password

---
