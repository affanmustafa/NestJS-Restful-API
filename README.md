# SnackMate - Backend

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Running the App](#running-the-app)
- [Development Workflow](#development-workflow)
- [Prisma Commands](#prisma-commands)
- [Contributing](#contributing)

## Introduction

This is a NestJS application using PostgreSQL as the database and Prisma as the ORM. This README provides instructions on how to set up the project, run the app, and contribute to the development.

## Prerequisites

- Node.js (v16 or above)
- PostgreSQL
- npm (v6 or above) or yarn

## Installation

1. Clone the repository:

```bash
git clone git@github.com:affanmustafa/NestJS-Restful-API.git
cd NestJS-Restful-API
```

2. Install dependencies:

```bash
npm install
```

or
```bash
yarn
```

## Database Setup

1. Create a `.env` file in the root directory and add your database URL:

```env
Contact the team for the environment variables
```

2. Run your Postgres database and populate the `DATABASE_URL` in the `.env` file. Another option is to use the provided `docker-compose.yml` to run Postgres in a docker container. To do this, run:

```bash
docker-compose up -d
```

Note: A sample `.env.test` has been provided in the project.

## Running the App

1. Start the application:

```bash
npm start:dev
```

2. By default, the application will be running on `http://localhost:8000`.

## Development Workflow

### Branching Model

- Create a new branch for your feature or fix from the `main` branch.

```bash
git checkout main
git pull origin main
git checkout -b feature/your-feature-name
```

- Commit your changes and push.
- Merge your branch into `main` branch.

```bash
git add .
git commit -m "Add feature or fix description"
git push origin feat/your-feature-name
```

- Create a pull request to merge your branch into `development`.

## Prisma Commands

- To apply database migrations:

```bash
npx prisma migrate dev --name "your-migration-name"
```

- To generate Prisma Client:

```bash
npx prisma generate
```

Please note that running migrations generates a new Prisma Client. Therefore, if you run a new migration, you do not need to run `npx prisma generate` again.

- To open Prisma Studio:

```bash
npx prisma studio
```
