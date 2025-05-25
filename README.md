# Start Kit

This project is a comprehensive starter kit designed for building modern, server-rendered web applications with a focus on a great developer experience and robust features. It integrates Vinxi as the bundler and server, React for the UI, TypeScript for type safety, TanStack Router for routing, TanStack Query for data fetching, and uses Radix UI components styled with Tailwind CSS for a flexible and modern UI.

It also includes a sample integration with Salesforce to demonstrate how to connect to external services.

## Features

*   **Framework**: Built with [Vinxi](https://vinxi.dev/) - a powerful and flexible bundler for web applications.
*   **UI Library**: [React](https://react.dev/) with [TypeScript](https://www.typescriptlang.org/) for building interactive and type-safe user interfaces.
*   **Routing**: [TanStack Router](https://tanstack.com/router) for type-safe routing.
*   **Data Fetching**: [TanStack Query](https://tanstack.com/query) for efficient data synchronization and caching.
*   **Styling**: [Tailwind CSS](https://tailwindcss.com/) for utility-first styling.
*   **UI Components**: A comprehensive set of UI components from [Radix UI](https://www.radix-ui.com/) and [Shadcn UI](https://ui.shadcn.com/), available in `app/components/ui/`.
*   **Tooling**: Uses [Vite](https://vitejs.dev/) under the hood via Vinxi, enabling a fast development experience.
*   **Example Integration**: Includes a sample Salesforce integration (`app/integrations/salesforce/`) to demonstrate connecting to external APIs.
*   **Development Environment**: Supports `bun` for package management and script execution.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   [Node.js](https://nodejs.org/) (LTS version recommended)
*   [Bun](https://bun.sh/) (Package manager and runtime)

### Installation

1.  Clone the repository:
    ```bash
    git clone <your-repository-url>
    cd start-kit 
    ```
2.  Install dependencies using Bun:
    ```bash
    bun install
    ```

### Running the Development Server

To start the development server, run:

```bash
bun run dev
```

This will start the Vinxi development server, typically available at `http://localhost:3000`.

### Building for Production

To create a production build, run:

```bash
bun run build
```

This command compiles and optimizes the application for production. The output will be in the `.output` directory.

### Starting the Production Server

After building the project, you can start the production server with:

```bash
bun run start
```

## Project Structure

The project follows a feature-oriented structure, making it easy to locate and manage different parts of the application.

```
.
├── app/                      # Core application code
│   ├── components/           # Shared React components
│   │   └── ui/               # UI components (Radix UI/Shadcn)
│   ├── hooks/                # Custom React hooks
│   ├── integrations/         # Example integrations (e.g., Salesforce)
│   │   └── salesforce/
│   ├── lib/                  # Utility functions and shared logic
│   ├── routes/               # TanStack Router route definitions and associated components
│   ├── styles/               # Global styles
│   ├── utils/                # General utility functions
│   ├── client.tsx            # Client-side entry point
│   ├── ssr.tsx               # Server-side rendering entry point
│   └── routeTree.gen.ts      # Generated route tree for TanStack Router
├── public/                   # Static assets (images, fonts, etc.)
├── .gitignore                # Files and directories to ignore for Git
├── app.config.ts             # Application configuration for Vinxi/TanStack Start
├── bun.lock                  # Bun lockfile
├── components.json           # Configuration for Shadcn UI (if used)
├── package.json              # Project metadata and dependencies
├── postcss.config.ts         # PostCSS configuration
├── tsconfig.json             # TypeScript configuration
└── README.md                 # This file
```

**Key Directories:**

*   **`app/`**: Contains all the core application logic.
    *   **`app/routes/`**: Defines the application's routes using TanStack Router. Each file or directory here typically corresponds to a URL path.
    *   **`app/components/`**: Houses reusable React components.
        *   **`app/components/ui/`**: Contains UI primitives and components, largely based on Radix UI and potentially customized via Shadcn UI.
    *   **`app/hooks/`**: For custom React hooks to encapsulate and reuse stateful logic.
    *   **`app/lib/`**: General utility functions, helper classes, or library-like code.
    *   **`app/integrations/`**: Provides examples or modules for integrating with third-party services, like the included Salesforce example.
*   **`public/`**: Stores static assets like images, fonts, or `favicon.ico` that are served directly.

## Salesforce Integration

This starter kit includes a sample integration with Salesforce, located in the `app/integrations/salesforce/` directory. This example is intended to demonstrate:

*   Connecting to the Salesforce API.
*   Fetching data from Salesforce.
*   Implementing both client-side and server-side logic for the integration.
*   Managing Salesforce sessions.

To understand the specifics of this integration, including configuration and usage, please explore the code within the `app/integrations/salesforce/` directory. You will find files related to API communication (`api.ts`), client-side setup (`client.ts`), server-side logic (under `server/`), and type definitions (`types.ts`).

This example can serve as a blueprint for building out more complex integrations with Salesforce or other third-party services.

## Customization

This starter kit is designed to be a foundation for your project. Here are a few areas you'll likely want to customize:

*   **UI Components**: The components in `app/components/ui/` are based on Shadcn UI and Radix UI. You can customize their appearance by modifying the Tailwind CSS classes or by following the Shadcn UI documentation for theming and component adjustments.
*   **Routing**: Modify and extend the application's routes by editing files within the `app/routes/` directory, following the conventions of TanStack Router.
*   **Styling**: Adjust global styles in `app/styles/app.css` or update the Tailwind CSS configuration (`tailwind.config.ts`) to change the design system.
*   **Integrations**: Remove or modify the example Salesforce integration in `app/integrations/salesforce/` and add your own integrations as needed.
*   **Content**: Update the placeholder content and components throughout the application to fit your project's requirements.

## License

This project is licensed under the ISC License. See the `LICENSE` file for more details (if one is present).
