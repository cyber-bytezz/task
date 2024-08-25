# Task Management App

![Task Management App Banner](https://github.com/user-attachments/assets/40d0efeb-85fe-441f-b11b-e4d442057204)

## Overview

The **Task Management App** is a comprehensive solution for managing tasks, built using **React.js** for the frontend, **MongoDB** for the database, **Prisma** for ORM, and **Clerk** for JWT-based authentication. It provides a seamless experience for users to manage their tasks effectively.

## Features

- **User Authentication**: Secure JWT-based authentication with **Clerk**.
- **Task Management**: Create, update, and delete tasks.
- **Dashboard**: Overview of tasks and project statuses.
- **Responsive Design**: Optimized for both mobile and desktop.
- **Role-Based Access**: Admin, project manager, and team member roles with different access levels.

## Tech Stack

| **Technology**  | **Description**                                      |
|-----------------|------------------------------------------------------|
| **React.js**    | Frontend library for building user interfaces       |
| **Next.js**     | Framework for server-side rendering and static site generation |
| **MongoDB**     | NoSQL database for data storage                     |
| **Prisma**      | ORM for database management and interaction          |
| **Clerk**       | Authentication solution for managing user sessions   |

## System Architecture

### Architecture Diagram
![Screenshot 2024-08-25 155135](https://github.com/user-attachments/assets/ef67798b-34c8-4355-8e05-019a3195fa1a)
![Screenshot 2024-08-25 155207](https://github.com/user-attachments/assets/5b5e0139-b2e5-4e91-993f-9421cb08560d)


The system architecture diagram illustrates the interaction between React.js, Next.js, MongoDB, Prisma, and Clerk, highlighting the flow of data and user authentication.

### Database Schema

![Screenshot 2024-08-25 160857](https://github.com/user-attachments/assets/0b2507e3-4369-4e58-b78f-859e0a4a805c)
![Screenshot 2024-08-25 161015](https://github.com/user-attachments/assets/8436776a-c849-4bca-9b86-bc31d346a053)

The database schema diagram provides an overview of the data structure used in MongoDB, including collections for users, tasks, and projects.

## Installation

### Prerequisites

- Node.js
- MongoDB
- Git

### Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**

   Create a `.env.local` file in the root directory with the following content:

   ```env
   DATABASE_URL="mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority"
   NEXT_PUBLIC_CLERK_FRONTEND_API="<your_clerk_frontend_api>"
   CLERK_API_KEY="<your_clerk_api_key>"
   JWT_SECRET="<your_jwt_secret>"
   ```

4. **Run the development server**

   ```bash
   npm run dev
   ```

   The app will be available at [http://localhost:3000](http://localhost:3000).

### Prisma Setup

If you make any changes to the Prisma schema, run:

```bash
npx prisma generate
```

To apply migrations:

```bash
npx prisma migrate dev
```

## Deployment

The app is deployed on Vercel. To deploy your own version:

1. Connect your GitHub repository to Vercel.
2. Set the environment variables in Vercel similar to your `.env.local` file.
3. Deploy the app.

## API Documentation

### Authentication Endpoints

- **POST /api/auth/register**: Register a new user.
- **POST /api/auth/login**: Log in a user and receive a JWT.
- **POST /api/auth/logout**: Log out the user.

### Task Management Endpoints

- **GET /api/tasks**: Retrieve all tasks.
- **POST /api/tasks**: Create a new task.
- **PUT /api/tasks/:id**: Update a task by ID.
- **DELETE /api/tasks/:id**: Delete a task by ID.


## Contributing

Contributions are welcome! Please fork the repository and create a pull request.

