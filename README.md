# Vite React App with Tailwind CSS and ShadCN Configuration

This guide will walk you through setting up a Vite React app with Tailwind CSS and ShadCN configuration using JavaScript (not TypeScript). Follow the steps below to get started.

## 1. Create a Vite App

Run the following commands to create a Vite React app:

```bash
npm create vite@latest
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
```
const greet = () => {
  console.log('Hello, world!');
};
```
