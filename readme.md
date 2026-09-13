# LinkForge

LinkForge is a full-stack web application built with **Express.js** and **React.js**.

## Tech stack

- **Frontend:** React.js
- **Backend:** Node.js and Express.js
- **Package manager:** npm
- **API style:** RESTful HTTP endpoints

## Project structure

The project is organized into separate frontend and backend applications:

```text
linkforge/
├── client/        # React.js frontend
├── server/        # Express.js backend and API
└── readm.md
```

## Prerequisites

Install the following before starting:

- Node.js 18 or later
- npm 9 or later

You can verify your installation with:

```bash
node --version
npm --version
```

## Installation

Clone the repository and install dependencies for both applications:

```bash
git clone <repository-url>
cd linkforge

cd server
npm install

cd ../client
npm install
```

## Environment variables

Create a `.env` file in the `server` directory. Add the values required by the backend, for example:

```env
PORT=5000
CLIENT_URL=http://localhost:3000
```

Do not commit `.env` files or other credentials to version control.

## Running locally

Start the Express.js API:

```bash
cd server
npm run dev
```

Start the React.js application in a second terminal:

```bash
cd client
npm start
```

The frontend is typically available at `http://localhost:3000`, and the API at `http://localhost:5000`.

## Available scripts

The exact scripts depend on the package configuration. A typical setup includes:

### Server

```bash
npm run dev      # Start the Express server with automatic reloads
npm start        # Start the server in production mode
npm test         # Run backend tests
```

### Client

```bash
npm start        # Start the React development server
npm run build    # Create a production build
npm test         # Run frontend tests
```

## API

The React frontend communicates with the Express backend through HTTP requests. Keep API routes grouped under a versioned prefix, such as:

```text
/api/v1/...
```

When adding an endpoint, document its method, URL, request body, response format, and possible error responses.

## Production build

Build the React frontend with:

```bash
cd client
npm run build
```

Configure the Express server and hosting platform according to the deployment environment. Set production environment variables through the hosting provider rather than committing them to the repository.

## Contributing

1. Create a feature branch.
2. Make focused changes and add tests where appropriate.
3. Run the client and server checks locally.
4. Open a pull request with a summary of the changes.

## License

Add the project license here.
