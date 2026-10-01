# SilverRoadCars

A full-stack car rental web application developed as a **four-person academic team project** at Brigham Young University–Idaho.

SilverRoadCars was built to manage vehicles, customers, staff users, bookings, rental requests, and vehicle maintenance within a single system.

## Live Demo

[View SilverRoadCars](https://silver-road-cars.onrender.com/)

## Features

The application includes:

- Vehicle browsing and rental workflows
- Customer registration and profiles
- Current and previous booking history
- Rental request management
- Staff and administrative areas
- Vehicle management
- Staff user management
- Vehicle maintenance workflows
- Authentication and protected routes
- Relational data stored in PostgreSQL
- Responsive web interface

## Tech Stack

| Area | Technologies |
| --- | --- |
| **Frontend** | `JavaScript` `EJS` `HTML` `CSS` |
| **Backend** | `Node.js` `Express.js` |
| **Database** | `PostgreSQL` |
| **Authentication** | `Express Session` `Passport` `Google OAuth` `JWT` `bcryptjs` |
| **Package Manager** | `pnpm` |
| **Collaboration** | `Git` `GitHub` `Trello` `Scrum` |
| **Deployment** | `Render` |

## My Contributions

As one of four developers working on SilverRoadCars, my contributions included:

- Implementing and improving full-stack application features
- Working with Node.js and Express backend routes
- Working with PostgreSQL queries and relational data
- Contributing to CRUD workflows across the application
- Building and refining administrative interface pages
- Working with JavaScript, EJS, HTML, and CSS on the frontend
- Testing features and fixing integration issues
- Collaborating with the team using Git, Scrum practices, and Trello

## Application Areas

### Customers

Customers can:

- Browse available vehicles
- Create and manage their profile
- Request vehicle rentals
- View current bookings
- View booking history

### Staff & Administration

Administrative functionality includes:

- Managing vehicles
- Managing staff users
- Working with bookings and rental information
- Supporting vehicle maintenance workflows

## Authentication

SilverRoadCars uses different authentication mechanisms across the application:

- `express-session` for server-side sessions
- Passport for authentication workflows
- Google OAuth through `passport-google-oauth20`
- JWT authentication for client sessions
- `bcryptjs` for password hashing

Authentication information is handled on the server and made available to the EJS views when needed.

## Database

SilverRoadCars uses PostgreSQL through the `pg` package and a connection pool.

The database configuration supports:

- A `DATABASE_URL` connection string for hosted environments such as Render
- Individual database variables for local development

SSL is automatically enabled when connecting to the hosted Render PostgreSQL database.

## Project Context

SilverRoadCars was developed for **CSE 499** at Brigham Young University–Idaho.

The application was completed by a team of four students over a six-week development period. The team worked collaboratively using Git and Trello, with development organized around shared responsibilities and iterative project work.

Unlike my individual portfolio project, Inventa, SilverRoadCars represents my experience contributing to a shared full-stack codebase and working as part of a development team.

## Running Locally

### Prerequisites

Make sure you have installed:

- Node.js
- pnpm
- PostgreSQL
- Git

### 1. Clone the repository

```bash
git clone <repository-url>
cd silverroadcars
```

### 2. Install dependencies

```bash
pnpm install
```

### 3. Configure environment variables

Create a `.env` file in the project root.

For a local PostgreSQL database:

```env
DB_USER="your-database-user"
DB_HOST="localhost"
DB_NAME="your-database-name"
DB_PASSWORD="your-database-password"
DB_PORT="5432"

PORT="3000"
SESSION_SECRET="your-session-secret"

GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
GOOGLE_CALLBACK_URL="http://localhost:3000/auth/google/callback"

JWT_SECRET="your-jwt-secret"
JWT_EXPIRES_IN="1d"
```

The application can also use a single PostgreSQL connection string:

```env
DATABASE_URL="your-postgresql-connection-string"
```

When `DATABASE_URL` is available, it is used instead of the individual database connection variables.

> Never commit `.env` files or real credentials to the repository.

### 4. Start the application

```bash
pnpm start
```

The application starts through the Express server configured in `./bin/www`.

By default, the local application is available at:

```text
http://localhost:3000
```

## Error Handling

The application includes:

- Custom handling for routes that are not found
- Centralized Express error handling
- Development-specific error details
- Safer production error responses
- A PostgreSQL connection health-check endpoint

## Deployment

SilverRoadCars is deployed on **Render** with a hosted PostgreSQL database.

Production environment variables and credentials are configured through the hosting platform rather than stored in the repository.

[View the live application](https://silver-road-cars.onrender.com/)

## Status

**Academic team project completed and deployed.**

The application is preserved as part of my software development portfolio and demonstrates my experience contributing to a collaborative full-stack project.
