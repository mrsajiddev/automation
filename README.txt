# Automation — Express.js CI/CD with GitHub Actions & Vercel

[![Deploy to Vercel](https://github.com/mrsajiddev/automation/actions/workflows/deploy.yml/badge.svg)](https://github.com/mrsajiddev/automation/actions/workflows/deploy.yml)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?logo=express&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?logo=vercel&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

A hands-on project demonstrating how to automate the deployment of an **Express.js application to Vercel using GitHub Actions**.

The goal is to build a simple, reliable CI/CD workflow where code changes pushed to the `main` branch automatically trigger a production deployment.

**Live Demo:** [View the deployed application](https://your-app.vercel.app) <!-- Replace with your actual Vercel URL -->

**Repository:** [mrsajiddev/automation](https://github.com/mrsajiddev/automation)

---

## Overview

This project explores the fundamentals of continuous integration and continuous deployment (CI/CD) by connecting GitHub, GitHub Actions, and Vercel.

### Key Features

- **Automated deployments** — Trigger production deployments when matching changes are pushed to `main`.
- **CI/CD with GitHub Actions** — Automate checkout, dependency installation, and deployment.
- **Express.js backend** — Serve HTTP routes and render dynamic or static UI pages.
- **Vercel hosting** — Deploy the application to a serverless hosting platform.
- **Secure credentials** — Store deployment tokens and project identifiers in GitHub Actions Secrets.
- **Repeatable workflow** — Keep deployment steps version-controlled alongside the application.

## CI/CD Workflow

text
Developer
   |
   | Push changes to main
   v
GitHub Repository
   |
   | Trigger workflow
   v
GitHub Actions
   |
   |-- Checkout repository
   |-- Setup Node.js
   |-- Install dependencies
   |-- Authenticate with Vercel
   |-- Deploy application
   |
   v
Vercel Production
   |
   v
Live Express.js Application

### Deployment Process

1. A developer commits and pushes changes to `main`.
2. GitHub Actions detects the push if it matches the configured workflow triggers.
3. The runner checks out the repository and prepares the Node.js environment.
4. The Vercel CLI authenticates using GitHub Secrets and deploys the application.
5. Vercel publishes the deployment to the configured production project.

> **Note:** Pull request preview deployments are not included unless explicitly configured in the workflow.

## Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime |
| Express.js | HTTP server and routing |
| EJS | Server-side HTML templating, if enabled |
| Git & GitHub | Source control and collaboration |
| GitHub Actions | Workflow automation |
| Vercel | Application hosting and deployment |
| npm | Dependency management |

## Project Structure

text
automation/
├── .github/
│   └── workflows/
│       └── vercel_deploy.yml       # GitHub Actions deployment workflow
├── 01-simple-blog/
│   ├── index.js             # Express application entry point
│   ├── package.json         # Project metadata and dependencies
│   ├── package-lock.json    # Locked dependency versions
│   ├── views/               # EJS templates, if configured
│   └── public/              # CSS, JavaScript and static assets
├── README.md
└── LICENSE

*The structure above reflects the application folder layout. Files such as `package-lock.json`, `views/`, `public/`, and `LICENSE` should be present only if you have created them.*

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 22 or a compatible supported version
- npm
- A GitHub account
- A Vercel account for deployment

### 1. Clone the Repository

bash
git clone https://github.com/mrsajiddev/automation.git
cd automation

### 2. Install Dependencies

bash
cd 01-simple-blog
npm install

### 3. Run Locally

bash
npm start


Open [http://localhost:3000](http://localhost:3000) in your browser.

## Deployment Setup

Follow these steps to configure automated deployment for your own Vercel project.

### 1. Create a Vercel Project

Create a project in the [Vercel Dashboard](https://vercel.com/dashboard) and link it to your GitHub repository.

Configure the **Root Directory** to match the location of your Express application. In this repository, that directory is `01-simple-blog`.

### 2. Generate a Vercel Token

Open your Vercel account settings and create an access token.

Keep this token private and never commit it to the repository.

### 3. Configure GitHub Secrets

Navigate to:

**GitHub Repository → Settings → Secrets and variables → Actions**

Add the following repository secrets:

| Secret | Description |
|---|---|
| `VERCEL_TOKEN` | Vercel access token |
| `VERCEL_ORG_ID` | Vercel account or team ID |
| `VERCEL_PROJECT_ID` | Vercel project ID |

The organization and project IDs can be obtained from the `.vercel/project.json` file created when linking a local project with the Vercel CLI.

### 4. Enable GitHub Actions

Ensure GitHub Actions is enabled for your repository and that the workflow exists at:

text
.github/workflows/deploy.yml


### 5. Deploy

Push a change to the `main` branch that matches the workflow's path filters:

bash
git add .
git commit -m "Update Express application"
git push origin main


Monitor the deployment from the repository's **Actions** tab.

After the workflow completes successfully, open your Vercel production URL to verify the application.

## Security Best Practices

- Keep all access tokens and credentials in GitHub Secrets.
- Never commit `.env` files or `.vercel` credentials to a public repository.
- Grant deployment tokens only the permissions they require.
- Avoid logging secrets in workflow output.
- Review deployment logs when a build or deployment fails.

## Roadmap

- [ ] Add automated API tests with Jest and Supertest.
- [ ] Add ESLint for consistent code quality.
- [ ] Add a test job that must pass before production deployment.
- [ ] Configure staging and production environments.
- [ ] Add deployment notifications and uptime monitoring.
- [ ] Add pull request preview deployments.
- [ ] Expand the Express application with additional routes and UI components.

## What I'm Learning

This project is part of my hands-on exploration of:

- CI/CD pipeline design
- GitHub Actions workflow configuration
- Node.js application deployment
- Vercel project configuration
- Environment variables and deployment secrets
- Automated delivery of web applications

## Author

**Muhammad Sajid** — Senior Software Engineer

- [LinkedIn](https://linkedin.com/in/mr-sajid)
- [GitHub](https://github.com/mrsajiddev)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.