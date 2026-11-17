# Linkforge

Linkforge is a web application built with **React** on the frontend and **Express.js** on the backend.

## Tech stack

- React for the user interface
- Express.js and Node.js for the API and server

## Getting started

### Prerequisites

- Node.js (LTS recommended)
- npm (included with Node.js)

### Install dependencies

Install the frontend and backend dependencies in their respective project directories:

```bash
cd client
npm install

cd ../server
npm install
```

### Run in development

Open separate terminals and start each part of the application using the scripts defined in its `package.json`:

```bash
# Terminal 1
cd server
npm run dev
```

```bash
# Terminal 2
cd client
npm run dev
```

If your project uses different directory names or script names, adjust these commands to match the `package.json` files.

## Project structure

The project is organized into a React frontend and an Express backend. A common layout is:

```text
Linkforge/
|-- client/   # React application
|-- server/   # Express API and server
```

## Configuration

Put environment-specific settings, such as the API port or database connection string, in environment variables. Keep secrets out of source control. Add required variable names and setup instructions here as the backend configuration is defined.

## Available scripts

See the `scripts` section of each `package.json` for the commands available to the frontend and backend.

