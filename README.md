# React App - Simple Setup & Deployment
---
![Deploy](https://github.com/dimasx010/puxurros/actions/workflows/deploy.yml/badge.svg)
![Made with React](https://img.shields.io/badge/React-18-blue?logo=react)
[![Website](https://img.shields.io/badge/Live_Site-Current_Time-blue?style=flat-square)](https://dimasx010.github.io/puxurros/)
---
This project was bootstrapped with **Puxurros React App** and focuses mainly on showcasing **deployment with GitHub Actions + GitHub Pages**.

---

## 🚀 Getting Started

### 📦 Install Dependencies

```bash
npm install
```

### ▶️ Run Development Server

```bash
npm start
```

* Opens your app at **[http://localhost:3000](http://localhost:3000)**
* Hot reload enabled

### 🧪 Run Tests

```bash
npm test
```

Runs Jest in watch mode.

### 📦 Create Production Build

```bash
npm run build
```

* Generates an optimized build in `/build`
* Minified, hashed filenames, ready for deployment

### ⚠️ Eject (Optional)

```bash
npm run eject
```

> **Warning:** This is irreversible.

This copies the internal Webpack/Babel/ESLint configs into your project for full customization.

---

## 📚 Learn More

* **CRA Docs:** [https://facebook.github.io/create-react-app/docs/getting-started](https://facebook.github.io/create-react-app/docs/getting-started)
* **React Docs:** [https://reactjs.org/](https://reactjs.org/)

Additional CRA guides:

* Code Splitting
* Analyzing Bundle Size
* Making a PWA
* Advanced Configuration
* Troubleshooting build errors

---

# 🚀 Deployment: GitHub Actions + GitHub Pages

This project’s main purpose is to demonstrate a clean CI/CD workflow for **automatic deployments** to GitHub Pages.

## 📂 Branch Strategy

* **main** → source code
* **gh-pages** → built static site (automatically updated)

## 🤖 GitHub Actions Workflow

A typical workflow file:

```yaml
name: Deploy React App

on:
  push:
    branches: ["main"]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Use Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install dependencies
        run: npm install

      - name: Build project
        run: npm run build

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./build
```

## 🔧 Project Configuration for GitHub Pages

In `package.json`, add:

```json
{
  "homepage": "https://<your-username>.github.io/<repository-name>/"
}
```

Then run:

```bash
npm run build
```

---

## 🎯 Summary

This repo is a simple React template but includes:

* Modern GitHub Actions CI/CD
* Automatic deployment to GitHub Pages
* Clean and maintainable workflow


---
![Deploy](https://github.com/dimasx010/puxurros/actions/workflows/deploy.yml/badge.svg)
![Made with React](https://img.shields.io/badge/React-18-blue?logo=react)
[![Website](https://img.shields.io/badge/Live_Site-Current_Time-blue?style=flat-square)](https://dimasx010.github.io/puxurros/)
---
