# Repository Guidelines

## Project Structure & Module Organization

LinkForge is intended to be a full-stack web app with a React frontend and an Express backend. Keep frontend code in `client/` and backend code in `server/` once those applications are scaffolded. Store React components near their feature code, shared frontend utilities under `client/src/`, and Express routes/controllers under `server/src/` or the closest existing backend pattern. Keep tests beside the code they verify or in a clear `tests/` directory within each app. Static assets should live in `client/public/` or `client/src/assets/`.

## Build, Test, and Development Commands

Install dependencies separately for each app:

```bash
cd server && npm install
cd ../client && npm install
```

Common development commands:

```bash
cd server && npm run dev    # start the Express API with reloads
cd client && npm start      # start the React development server
cd client && npm run build  # create a production frontend build
npm test                    # run tests from the current app directory
```

Check each app's `package.json` before adding or changing scripts.

## Coding Style & Naming Conventions

Use JavaScript or TypeScript consistently within each app. Prefer 2-space indentation, semicolons only if the local files already use them, and descriptive names over abbreviations. React components should use `PascalCase` filenames, such as `LinkCard.jsx`; hooks should start with `use`, such as `useLinks.js`; backend route files should use lower-case, purpose-based names such as `links.routes.js`.

## Testing Guidelines

Add tests for new user-facing behavior, API endpoints, and bug fixes. Frontend tests should typically use React Testing Library with Jest or Vitest. Backend tests should exercise Express routes and service logic with Jest, Vitest, or Supertest. Name tests after the unit or feature being verified, for example `LinkCard.test.jsx` or `links.routes.test.js`.

## Commit & Pull Request Guidelines

Current history uses short imperative commits, for example `Add project README`. Continue that style: `Add link creation API`, `Fix dashboard empty state`, or `Update client build script`. Pull requests should include a short summary, testing notes, linked issues when relevant, and screenshots for visible UI changes.

## Security & Configuration Tips

Keep secrets out of git. Store backend configuration in `server/.env`, such as `PORT=5000` and `CLIENT_URL=http://localhost:3000`, and document required variables without committing real credentials.
