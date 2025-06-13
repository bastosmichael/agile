# Agile

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Agile is a project management platform inspired by Jira. It helps teams track work across workspaces, projects and tasks while providing clear analytics. Built with Next.js and Appwrite, Agile offers a modern interface with drag-and-drop boards, calendars and role-based collaboration.

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Setup](#setup)
  - [Simple Mode Setup](#simple-mode-setup)
  - [Advanced Mode Setup](#advanced-mode-setup)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [FAQ](#faq)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Features

- Email and password authentication with Appwrite
- Multi-workspace structure with invite codes and role management
- Projects and tasks with Kanban, table and calendar views
- Drag-and-drop task board with bulk updates
- Analytics endpoints for projects and workspaces
- Dark mode and responsive UI built with Tailwind CSS and Radix UI

## Demo

*Coming soon*

## Setup

Both modes assume Node.js and npm are installed.

### Simple Mode Setup

1. **Clone the Repository**
   ```bash
   git clone [repo-url]
   cd [project-name]
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Configure Environment**
   ```bash
   cp .env.example .env.local
   ```
   Required variables:
   * `APP_MODE=simple`
   * `NEXT_PUBLIC_APPWRITE_ENDPOINT=`
   * `NEXT_PUBLIC_APPWRITE_PROJECT=`
   * `NEXT_PUBLIC_APPWRITE_DATABASE_ID=`
   * `NEXT_PUBLIC_APPWRITE_WORKSPACES_ID=`
   * `NEXT_PUBLIC_APPWRITE_MEMBERS_ID=`
   * `NEXT_PUBLIC_APPWRITE_PROJECTS_ID=`
   * `NEXT_PUBLIC_APPWRITE_TASKS_ID=`
   * `NEXT_PUBLIC_APPWRITE_IMAGES_BUCKET_ID=`
   * `NEXT_APPWRITE_KEY=`
   
4. **Run the App**
   ```bash
   npm run dev
   ```

### Advanced Mode Setup

Use advanced mode if you want to self‑host Appwrite or customize infrastructure.

1. Provision an Appwrite instance and create the database and storage buckets listed in `.env.example`.
2. Fill the environment variables above with your instance details and admin key.
3. Build for production:
   ```bash
   npm run build
   npm start
   ```

## Usage

1. Register or log in.
2. Create a workspace and invite team members via invite code.
3. Inside a workspace create projects and start adding tasks.
4. Switch between table, kanban and calendar views to manage tasks.
5. View analytics for workspaces or projects to monitor progress.

## Deployment

The project is ready for platforms like Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import)

1. Fork this repository and push it to your Git provider.
2. Press **Deploy with Vercel** and follow the prompts.
3. Set environment variables in Vercel using the values from your `.env.local`.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## FAQ

**How do I reset my workspace invite code?** Use the `/reset-invite-code` endpoint from the API or the corresponding button in the UI.

**Can I downgrade my own role?** The last admin of a workspace cannot remove or downgrade themselves to prevent lockout.

**Does the app support dark mode?** Yes. Theme toggling is handled via `next-themes` and Tailwind CSS classes.

## License

This project is licensed under the MIT license.

## Acknowledgements

- [Next.js](https://nextjs.org)
- [Appwrite](https://appwrite.io)
- [Hono](https://hono.dev)
- [Radix UI](https://www.radix-ui.com)
- [Tailwind CSS](https://tailwindcss.com)
- [React Query](https://tanstack.com/query)

## Contact

Please open an issue in this repository to reach the maintainers.

