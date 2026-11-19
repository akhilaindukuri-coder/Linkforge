# Repository Guidelines

## Project Structure & Module Organization

Linkforge is a URL shortener with a React 18/Vite client and an Express API, managed as npm workspaces. Keep browser code in `client/`, API routes and JSON-file persistence in `server/`, and API integration tests in `tests/`. The server persists sample and user-created links in `server/data/links.json`; generated client output belongs in `client/dist/` and should not be edited by hand. The root `README.md` documents the API contract and local setup.

## Build, Test, and Development Commands

Run commands from the repository root:

- `npm install` installs workspace dependencies.
- `npm run dev` starts the API and Vite development server (ports 4000 and 5173 by default).
- `npm test` runs API integration tests with Node's built-in test runner.
- `npm run build` builds the client into `client/dist/`.
- `npm start` starts the Express API only.

Use Node.js 18 or later. The development client proxies `/api` and `/r` to the API. Configure `PORT`, `LINKS_FILE`, and `PUBLIC_ORIGIN` as described in the README.

## Coding Style & Naming Conventions

Follow the existing JavaScript conventions in each workspace. Use two spaces for indentation, semicolons, and descriptive camelCase names for variables and functions. Use PascalCase for React components and keep component files named for their primary component. Keep API endpoints and response shapes consistent with the README; validate inputs at the API boundary and preserve the JSON store's established link fields. No formatter or linter is currently documented, so avoid introducing one without a project need.

## Testing Guidelines

Add API integration tests under `tests/` using Node's built-in `node:test` runner and assert behavior through HTTP requests to the exported Express app. Use the in-memory store for tests so persisted sample data remains untouched. Run `npm test` after changes that affect API behavior or persistence. The repository does not document a coverage threshold.

## Commit & Pull Request Guidelines

No Git history or pull request template is available in this checkout to establish project-specific conventions. Write short, imperative commit subjects (for example, `Add tag filtering`) and keep changes focused. Pull requests should explain the user-visible change, list relevant validation (such as `npm test` and `npm run build`), link any related issue, and include screenshots for UI changes.

## Security & Configuration

Only public `http` and `https` destination URLs are accepted. The starter has no accounts or access control; do not expose private links publicly without adding authentication. Keep local secrets out of source control and use environment variables for runtime configuration.
