# nextjs-starter-pack

following along next js documentation as a study purpose as a quick way to start learning and development using next.

## getting started section

- installing a new package manager, recommended by vercel
- creating a next.js app using npm and using an example template.

installing pnpm:

    npm install -g pnpm
    
running the code:

    npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm

This templates is an already on-going project, so, this means that the main purpose of it is to learn all next.js main features without having to write all the application code.

### project structure

Before advancing to the actual development and coding phase, I need to spend some time to learn about project structure, because it has changed from src structure to app structure (latest next.js versions).

#### App

Contains all the routes, components, and logic for your application, this is where you'll be mostly working from.

#### App/lib

Contains functions used in your application, such as reusable utility functions and data fetching functions.

#### App/ui

Contains all the UI components for your application, such as cards, tables, and forms. To save time, we've pre-styled these components for you.

#### public

Contains all the static assets for your application, such as images.

#### Config files

Notice config files such as next.config.js at the root of your application. Most of these files are created and pre-configured when you start a new project using create-next-app.