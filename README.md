# Next.js App Router Dashboard

## Project Overview

This project is a comprehensive dashboard application built by following the official **[Next.js App Router Course](https://nextjs.org/learn)** provided by Vercel. It serves as a hands-on learning experience to master the core concepts and new features of Next.js, including the App Router, Server Components, and Server Actions.

The application is a full-featured invoice management dashboard. It allows users to log in, view a summary of revenue and recent invoices, manage customers, and perform full CRUD (Create, Read, Update, Delete) operations on invoices.

## Key Features & Concepts Covered

This project demonstrates a wide range of modern web development practices and Next.js features:

-   **Next.js App Router:**
    -   **File-based Routing:** Structuring the application with the `app/` directory.
    -   **Layouts:** Creating shared UI with `layout.tsx`.
    -   **Route Groups:** Organizing routes without affecting the URL path using parentheses, like `(overview)`.
    -   **Dynamic Routes:** Building pages for specific items, such as `invoices/[id]/edit`.

-   **Data Fetching & Management:**
    -   **Server Components:** Fetching data directly from a PostgreSQL database on the server using `async`/`await`.
    -   **Streaming & Suspense:** Implementing instant loading states with `loading.tsx` and the `<Suspense>` component to improve user experience while data is being fetched.
    -   **Server Actions:** Handling form submissions and data mutations (`create`, `update`, `delete`) securely on the server, with progressive enhancement.

-   **User Experience & Interactivity:**
    -   **Search & Pagination:** Implementing server-side search and pagination for invoice data.
    -   **Authentication:** Implementing user login/logout and protecting routes using `NextAuth.js` and `middleware`.
    -   **Error Handling:** Gracefully managing errors with `error.tsx` and creating 404 pages with `not-found.tsx`.
    -   **UI Skeletons:** Providing loading skeletons to give users immediate feedback.

-   **Styling & Development:**
    -   **Styling:** Utilizing **Tailwind CSS** for a modern, responsive design and `clsx` for conditional class names.
    -   **TypeScript:** Ensuring type safety across the entire application with strongly-typed definitions in `definitions.ts`.
    -   **Database Seeding:** A route-based script (`/app/seed/route.ts`) to populate the database with initial placeholder data.
    -   **Form Validation:** Using **Zod** for robust server-side form validation.

## Technology Stack

-   **Framework:** [Next.js](https://nextjs.org/)
-   **Language:** [TypeScript](https://www.typescriptlang.org/)
-   **Styling:** [Tailwind CSS](https://tailwindcss.com/)
-   **UI Icons:** [Heroicons](https://heroicons.com/)
-   **Authentication:** [NextAuth.js](https://next-auth.js.org/)
-   **Database:** [Vercel Postgres](https://vercel.com/storage/postgres)
-   **Validation:** [Zod](https://zod.dev/)

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

-   Node.js and pnpm (or npm/yarn) installed.
-   A Vercel account with a Postgres database created.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2.  **Install dependencies:**
    ```bash
    pnpm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of your project and add your Vercel Postgres connection string and an `AUTH_SECRET`.
    ```env
    POSTGRES_URL="your-postgres-url-from-vercel"
    AUTH_SECRET="your-secret-for-nextauth"
    ```
    You can generate a secret for `AUTH_SECRET` by running `openssl rand -base64 32` in your terminal.

4.  **Seed the database:**
    Once the application is running, the database tables and initial data can be seeded by navigating to the `/seed` route in your browser.
    ```
    http://localhost:3000/seed
    ```
    This will execute the code in `app/seed/route.ts` and populate your database.

5.  **Run the development server:**
    ```bash
    pnpm dev
    ```
    Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Acknowledgments

This project was built as part of the official **[Next.js Learn Course](https://nextjs.org/learn)**. All credit for the course material, structure, and concepts goes to the Vercel and Next.js team.
