# 🎵 Music Microservice Project

A microservice-based music application consisting of multiple backend
services and a React + Vite frontend.

Each backend service is an independent TypeScript Node project, and the
frontend is built using React, Tailwind CSS, and Vite.

------------------------------------------------------------------------

## 📂 Project Structure

    spotify-microservice-project-2025/
    │
    ├── admin service/
    │
    ├── user service/
    │
    ├── song service/
    │
    └── frontend/

------------------------------------------------------------------------

## 🛠️ Tech Stack

### Backend (Microservices)

-   Node.js
-   TypeScript
-   Nodemon
-   Concurrently

Backend script behavior:

    build  -> tsc
    start  -> node dist/index.js
    dev    -> concurrently "tsc -w" "nodemon dist/index.js"

------------------------------------------------------------------------

### Frontend

-   React 19
-   Vite
-   TypeScript
-   Tailwind CSS
-   React Router DOM
-   Axios
-   React Hot Toast

Frontend script behavior:

    dev      -> vite
    build    -> tsc -b && vite build
    preview  -> vite preview

------------------------------------------------------------------------

## ⚙️ Requirements

-   Node.js 18 or above
-   npm / yarn / pnpm

------------------------------------------------------------------------

## 🚀 Installation & Setup

Clone the project and install dependencies in each module.

------------------------------------------------------------------------

### 1️⃣ Admin Service

``` bash
cd "admin service"
npm install
npm run dev
```

Build

``` bash
npm run build
```

Start (production)

``` bash
npm start
```

------------------------------------------------------------------------

### 2️⃣ User Service

``` bash
cd "../user service"
npm install
npm run dev
```

------------------------------------------------------------------------

### 3️⃣ Song Service

``` bash
cd "../song service"
npm install
npm run dev
```

------------------------------------------------------------------------

### 4️⃣ Frontend

``` bash
cd ../frontend
npm install
npm run dev
```

Build

``` bash
npm run build
```

Preview production build

``` bash
npm run preview
```

------------------------------------------------------------------------

## 🔐 Environment Variables

Create a `.env` file in each backend service.

Example:

    PORT=5000
    DATABASE_URL=
    JWT_SECRET=

Frontend example:

    VITE_API_BASE_URL=http://localhost:5000

------------------------------------------------------------------------

## ▶️ Recommended Run Order

Start backend services first:

    admin service  → npm run dev
    user service   → npm run dev
    song service   → npm run dev

Then start frontend:

    frontend → npm run dev

------------------------------------------------------------------------

## 📌 Scripts Summary

### Backend

  Command         Description
  --------------- ------------------------
  npm run build   Compile TypeScript
  npm run start   Run compiled output
  npm run dev     Watch + nodemon reload

------------------------------------------------------------------------

### Frontend

  Command           Description
  ----------------- ---------------------
  npm run dev       Run Vite dev server
  npm run build     Production build
  npm run preview   Preview build
  npm run lint      Run ESLint

------------------------------------------------------------------------

## 🧾 Notes

-   Each service runs independently
-   `dist/` is generated after build
-   Dev mode uses TypeScript watch mode + Nodemon

------------------------------------------------------------------------

## 📜 License

This project is for learning and development purposes.
