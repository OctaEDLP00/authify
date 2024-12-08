# authify
Authify is a secure user management API built with Node.js and TypeScript. It provides JWT authentication, role-based permissions, email verification, and access auditing, making it scalable and customizable for any project.

# Authify  

Authify is a modern and secure API for user management and authentication. Built with Node.js and TypeScript, it provides a scalable and flexible solution to handle roles, permissions, and authentication flows for web applications.  

## Key Features  
- **JWT Authentication**: Secure, stateless session management.  
- **Roles and Permissions**: Support for hierarchical and customizable roles.  
- **Email Verification**: Account confirmation via unique email links.  
- **Password Recovery**: Secure links to reset forgotten passwords.  
- **Auditing**: Access logs for better security and user monitoring.  
- **Modular Design**: Easy to customize and extend for any project.  

---

## Technologies Used  
- **Node.js**  
- **Express.js**  
- **TypeScript**  
- **JWT (JSON Web Tokens)**  
- **bcrypt** for password hashing.  
- **Nodemailer** for email delivery.  
- **PostgreSQL** (or optionally MongoDB) as the database.  

---

## Installation  

1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/Authify.git
   cd Authify
   ```

2. Install dependencies
   ```bash
   npm install #or pnpm yarn bun or deno
   ```

3. Set up environment variables:
Create a .env file in the root directory with the following keys:
  ```env
  Copiar código
  PORT=3000
  DATABASE_URL=postgresql://username:password@localhost:5432/authify
  JWT_SECRET=your_secret
  SMTP_HOST=smtp.example.com
  SMTP_PORT=587
  SMTP_USER=your_email
  SMTP_PASSWORD=your_password
  ```

4. Start the application:

```bash
npm run dev
```

## Main Endpoints

### Authentication

POST /auth/register
Register a new user.

POST /auth/login
Log in and receive a JWT token.

POST /auth/forgot-password
Send a password reset link.

POST /auth/reset-password
Set a new password.

### User Management

GET /users
List all users (admin only).

GET /users/:id
Get details of a specific user.

PUT /users/:id
Update user information.

DELETE /users/:id
Delete or deactivate a user.

## Available Scripts

npm run dev: Start the server in development mode.
npm run build: Build the project for production.
npm start: Start the server in production mode.
npm run lint: Check the code for style and syntax issues.
