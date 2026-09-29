# Job Management Application

A small React and TypeScript kanban board for organizing jobs through three stages: **To Do**, **In Progress**, and **Completed**. Add a job with notes and categories, then search, edit, delete, or drag it between stages.

## Features

- Create jobs with a title, status, notes, and up to three categories.
- Search jobs by title, notes, category, or status.
- Edit job titles and notes, reveal notes on demand, and delete jobs with confirmation.
- Drag jobs between the To Do, In Progress, and Completed columns.
- Persist jobs in the browser with `localStorage`, so data remains after a page refresh.
- Use Bun's development server with hot reloading.

## Tech stack

- [React](https://react.dev/) 19
- [TypeScript](https://www.typescriptlang.org/)
- [Bun](https://bun.com/) for package management, development, and production serving
- Plain CSS for the interface

## Getting started

### Prerequisites

Install [Bun](https://bun.com/docs/installation) 1.3 or newer.

### Install dependencies

From the repository root:

```bash
bun install
```

### Start the development server

```bash
bun dev
```

Open the URL printed by Bun in your browser. The development server enables hot reloading while you edit files in `src/`.

### Build and run for production

Create an optimized browser bundle:

```bash
bun run build
```

Start the application with the production server:

```bash
bun start
```

## Using the application

1. Enter a job title and notes.
2. Select a status and at least one category.
3. Select **Add to To Do** to create the job.
4. Search from the search bar, or use **Clear** to remove the current search.
5. Drag a job card to another column to change its status.
6. Use **Edit** to update a title or notes, and use the delete icon to remove a job.
7. Use **Clear All Jobs** to remove every saved job from the browser.

Jobs are stored locally under the `jobs` `localStorage` key. They are not sent to a backend, so each browser profile has its own data.

## Project structure

```text
.
├── src/
│   ├── components/       Form, kanban columns, and job card components
│   ├── images/            Status and action icons
│   ├── App.tsx            Job state, filtering, persistence, and board layout
│   ├── frontend.tsx       React entry point
│   └── index.ts           Bun server entry point
├── package.json           Bun scripts and runtime dependencies
├── tsconfig.json          TypeScript configuration
└── bunfig.toml            Bun environment configuration
```

## Contributing

The project is maintained by [VoidLance](https://github.com/VoidLance). Contributions are welcome:

1. Open an issue describing a bug or proposed improvement.
2. Create a focused branch from the current default branch.
3. Make the smallest change that addresses the issue.
4. Run the available checks locally, including `bun run build`.
5. Open a pull request with a clear summary and testing notes.

Please keep changes focused and follow the existing TypeScript, React, and CSS patterns.

## Getting help

For questions, bug reports, or feature requests, use the repository's [GitHub Issues](https://github.com/VoidLance/course-files-javascript-react-job-management-application-form/issues).

## License

No license file is currently included in this repository. Add or consult the project's licensing terms before redistributing it.
