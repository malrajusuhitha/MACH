# MACH Project Documentation

## Overview

MACH2 is a full-stack project consisting of a client-side React application and a server-side Node.js API. The project is structured to efficiently manage UI components, API controllers, and routing logic.

## Table of Contents

- [Installation](#installation)
- [Project Structure](#project-structure)
- [Client Side](#client-side)
  - [Main Files](#main-files)
  - [Utilities](#utilities)
  - [Environment Variables](#environment-variables)
- [Server Side](#server-side)
  - [Controllers](#controllers)
  - [Routes](#routes)
- [Usage Examples](#usage-examples)

## Installation

To set up the project, clone the repository and install dependencies:

```sh
git clone <https://github.com/malrajusuhitha/MACH>
cd MACH2
```

### Installing Client Dependencies
```sh
cd client
npm install
npm run dev
```

### Installing Server Dependencies
```sh
cd server
npm install
npm run dev
```

## Project Structure

```
MACH2/
├── client/
│   ├── src/
│   │   ├── lib/
│   │   ├── pages/
│   │   │   ├── HomePage.tsx
│   │   ├── utils/
│   │   │   ├── types.ts
│   │   ├── App.tsx
│   │   ├── config.ts
│   │   ├── index.css
│   │   ├── main.tsx
│   │   ├── vite-env.d.ts
│   ├── .env
│   ├── package.json
│   ├── vite.config.ts
├── server/
│   ├── src/
│   │   ├── controllers/
│   │   │   ├── aiControllers.ts
│   │   ├── routes/
│   │   │   ├── aiRouters.ts
│   │   │   ├── index.ts
│   ├── .env
│   ├── package.json
│   ├── tsconfig.json
```

## Client Side

The client-side application is built with React, TypeScript, and Vite.

### Main Files
- **App.tsx** - The main entry point for the React application.
- **main.tsx** - Renders the React application and injects it into the root element.
- **index.css** - Contains global styles for the application.

### Utilities
- **types.ts** - Defines TypeScript types used across the application.
- **config.ts** - Stores configuration variables for the application.

### Environment Variables
- **.env** - Contains environment-specific variables.
- **.env.example** - A sample environment configuration file.

## Server Side

The server-side application is built using Node.js and Express with TypeScript.

### Controllers
- **aiControllers.ts** - Defines API logic for handling AI-related requests.

### Routes
- **aiRouters.ts** - Defines routes related to AI services.
- **index.ts** - Entry point for setting up Express routes.

## Usage Examples

### Example Client Component
```tsx
import { Button } from "@/components/ui/button";

function HomePage() {
  return (
    <div>
      <Button variant="default">Click Me</Button>
    </div>
  );
}
export default HomePage;
```

### Example API Route
```ts
import express from 'express';
import { aiController } from '../controllers/aiControllers';

const router = express.Router();
router.get('/ai', aiController);
export default router;
```

This documentation provides a detailed step-by-step guide to understanding the MACH2 project.

