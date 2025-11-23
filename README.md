# 💬 Real-Time Communication Platform

This is a modern, full-stack, real-time communication platform designed for instant messaging, voice, and video chat, demonstrating proficiency in the T3 stack and WebSocket integration.

The project is built around the concepts of servers, channels, and members, providing a complete chat application experience.

## 🚀 Key Features

* **Real-Time Messaging:** Instantaneous text message updates and deletion across all channels using **Socket.io** (WebSockets).
* **Voice and Video Channels:** Integrated media rooms for audio and video communication powered by **LiveKit**.
* **Authentication:** Secure user sign-in and sign-up powered by **Clerk**.
* **Server Management:** Users can create, manage, and invite members to custom servers and channels (text, audio, video).
* **File Sharing:** Securely upload and share files (images, documents) within chat channels using **UploadThing**.
* **Database:** Structured data persistence using **Prisma ORM** with a **PostgreSQL** backend.
* **Modern UI/UX:** Responsive, aesthetic user interface built with **Tailwind CSS** and **Shadcn UI**.
* **Infinite Scrolling:** Efficiently load and display message history using infinite scrolling queries.

## ⚙️ Technologies Used

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Full-Stack** | **Next.js 14+** (App Router) | High-performance React framework for server-side and client-side logic. |
| **Database ORM** | **Prisma** | Next-generation ORM for simplified database access and migrations. |
| **Real-Time** | **Socket.io** & **LiveKit** | WebSockets for instant chat and LiveKit for real-time media rooms. |
| **Authentication** | **Clerk** | Secure and flexible user authentication and management. |
| **Styling** | **Tailwind CSS** & **Shadcn UI** | Utility-first CSS framework for rapid and responsive styling. |
| **File Upload** | **UploadThing** | Streamlined file handling and storage solution. |
| **Language** | **TypeScript** | For type safety and better developer experience. |

## 🛠️ Setup and Installation Guide

To run this application locally, you need to set up several services and configure environment variables.

### Prerequisites

* Node.js (LTS recommended) and npm/yarn/pnpm
* A running PostgreSQL or compatible database instance.
* Accounts for Clerk, LiveKit, and UploadThing to obtain API keys.

### 1. Environment Configuration

```bash
Create a file named `.env.local` in the root directory and populate it with your keys (referencing the `.env.example` file):

DATABASE_URL="YOUR_POSTGRES_DATABASE_URL"

CLERK_SECRET_KEY="YOUR_CLERK_SECRET_KEY"
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="YOUR_CLERK_PUBLISHABLE_KEY"

UPLOADTHING_SECRET="YOUR_UPLOADTHING_SECRET"
UPLOADTHING_APP_ID="YOUR_UPLOADTHING_APP_ID"

LIVEKIT_API_KEY="YOUR_LIVEKIT_API_KEY"
LIVEKIT_SECRET="YOUR_LIVEKIT_SECRET"
NEXT_PUBLIC_LIVEKIT_URL="YOUR_LIVEKIT_URL"

NEXT_PUBLIC_SITE_URL="http://localhost:3000"
```

### 2. Database Setup

1.  Install the project dependencies:
    ```bash
    npm install
    ```
2.  Push the Prisma schema to your database (this creates the tables):
    ```bash
    npx prisma db push
    ```
3.  Generate the Prisma client:
    ```bash
    npx prisma generate
    ```

### 3. Run the Application

Start the development server:

```bash
npm run dev
```
The application will be accessible at http://localhost:3000.



