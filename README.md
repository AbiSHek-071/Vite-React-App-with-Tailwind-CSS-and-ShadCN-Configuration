# Vite React App with Tailwind CSS and ShadCN Configuration

This guide will walk you through setting up a Vite React app with Tailwind CSS and ShadCN configuration using JavaScript (not TypeScript). Follow the steps below to get started.

## 1. Create a Vite App

Run the following commands to create a Vite React app:

```bash
npm create vite@latest
```
```
# Package name: your-app-name
# Select a framework: React
# Select a variant: JavaScript
```

Navigate to the vite app and install the depadencies 
```bash
cd your-app-name
npm install
```
## 2. Tailwind installation 
Enter these commands in the terminal and hit enter 
```
npm install tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
Now,there will be tailwind.config.js file in the root folder of the project director edit it to this 

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './index.html',
    './src/**/*.{js,jsx,ts,tsx}', // This makes sure Tailwind CSS can process all your React components
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Like that there will be index.css file inside the src folder edit it and add this at the top

```css
/* src/index.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## 3. Shadcn installation

First look for a jsconfig.json file in the root of the project directory.Probebly there is not one, so create one. 
Inside it add this and save 

```json
{
  "compilerOptions": {
    // ...
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"]
    }
    // ...
  }
}
```

Now open the vite.config.js and edit it, add this and save 
```js
import { defineConfig } from 'vite'
import path from "path";
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src"),
    },
  },
});
```
Now let's enter the commands in the terminal and finish it off.
Enter the two command and hit enter.

```
npm install -D @types/node
npx shadcn@latest init
```

## That's it you created a Vite React app with tailwind css and shadcn configured in Javascript (again not Typescript).
Now try adding a Shadcn <Button/>. If you don't know it, ask chatgpt or go to the shadcn website and find it your own.....


