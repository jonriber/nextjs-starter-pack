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

### placeholder data

When build user interfaces, it helps and it is a very good development practice to have placeholder data or mock data.

Usually, when a database or API is not yet available.


### TypeScript

Typescript usage on this project reflects the modern web development landscape.

It is a javascript extension, adding typing into development.

here it is a good example of it:

    export type Invoice = {
        id: string;
        customer_id: string;
        amount: number;
        date: string;
        // In TypeScript, this is called a string union type.
        // It means that the "status" property can only be one of the two strings: 'pending' or 'paid'.
        status: 'pending' | 'paid';
        };

So, typescript usage ensure we don´t accidentally pass the wrong data format to react components or database entity. One example:

- passing a `string` instead of a `number` to invoice `amount`

### Running development server

Like `npm`, `pnpm` is used to install project dependencies.

Continuing on `nextjs-dashboard` folder, where package file is at, run:

    pnpm i

Then, to start development server on port 3000 (default port):

    pnpm dev

## CSS styling

Now, learning about different ways to style my `Next.js` application.

### Global styles

Inside the folder `/app/ui` there is a file named `global.css`. This is where you add CSS rules to all application routes.

So, you can import this file into any component available on the app. But is a very good development practice to import this into a top-level component (entry point).

Adding global styles to my application by importing this file on `/app/layout.tsx`.

    import '@/app/ui/global.css';
 
    export default function RootLayout({
        children,
    }: {
        children: React.ReactNode;
    }) {
        return (
            <html lang="en">
            <body>{children}</body>
            </html>
        );
    }