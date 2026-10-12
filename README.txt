# Automation: Express App with CI/CD to Vercel

[![Deploy to Vercel](https://github.com/mrsajiddev/automation/actions/workflows/deploy.yml/badge.svg)](https://github.com/mrsajiddev/automation/actions/workflows/deploy.yml)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)

A single-page application served by **Express.js**, with a fully automated deployment pipeline. Every push to `main` is built and deployed to **Vercel** through **GitHub Actions**, with no manual steps.

🔗 **Live demo:** [your-app.vercel.app](https://your-app.vercel.app)

---

## Why this project

Manual deployments are slow and easy to get wrong. This repository shows a simple, production-style workflow where shipping a change is as easy as merging a pull request:

- **Push to `main`**: the app is deployed to production automatically
- **Open a pull request**: a preview deployment is created so changes can be reviewed live before merging
- **Secrets stay safe**: Vercel credentials live in GitHub Secrets, never in the code

---

## How the pipeline works

```
 Developer          GitHub              GitHub Actions             Vercel
     │                 │                       │                      │
     │── git push ────▶│                       │                      │
     │                 │── triggers workflow ─▶│                      │
     │                 │                       │── install & build    │
     │                 │                       │── deploy ───────────▶│
     │                 │                       │                      │── app is live 🚀
```

1. Code is pushed to GitHub, or a pull request is opened.
2. GitHub Actions checks out the code and installs dependencies.
3. The Vercel CLI pulls the project settings, builds the app and deploys it.
4. Pushes to `main` go to **production**. Pull requests get a **preview URL**.

---

## Tech stack

| Layer            | Technology                    |
| ---------------- | ----------------------------- |
| Runtime          | Node.js                       |
| Server           | Express.js                    |
| Frontend         | Single-page application (SPA) |
| CI/CD            | GitHub Actions                |
| Hosting          | Vercel                        |
| Version control  | Git & GitHub                  |

---

## Project structure

```
automation/
├── .github/
│   └── workflows/
│       └── deploy.yml      # CI/CD pipeline: build and deploy to Vercel
├── public/                 # Static assets for the SPA (HTML, CSS, JS)
├── index.js                # Express server entry point
├── vercel.json             # Vercel routing and build configuration
├── package.json
└── README.md
```

---

## Getting started

### Prerequisites

- [Node.js](https://nodejs.org/) 18 or later
- npm

### Run locally

```bash
# Clone the repository
git clone https://github.com/mrsajiddev/automation.git
cd automation

# Install dependencies
npm install

# Start the server
npm start
```

Then open **http://localhost:3000** in your browser.

---

## Setting up the deployment

To run this pipeline in your own fork:

1. **Create a Vercel project** and link it locally:
   ```bash
   npm i -g vercel
   vercel link
   ```
   This creates `.vercel/project.json`, which contains your `orgId` and `projectId`.

2. **Generate a Vercel token** from *Vercel → Account Settings → Tokens*.

3. **Add these secrets** in *GitHub → Settings → Secrets and variables → Actions*:

   | Secret              | Where to find it            |
   | ------------------- | --------------------------- |
   | `VERCEL_TOKEN`      | Vercel account tokens page  |
   | `VERCEL_ORG_ID`     | `.vercel/project.json`      |
   | `VERCEL_PROJECT_ID` | `.vercel/project.json`      |

4. **Push to `main`.** The workflow runs and your app goes live.

---

## Roadmap

- [ ] Add automated tests (Jest + Supertest) as a required step before deploying
- [ ] Add linting with ESLint in the pipeline
- [ ] Add environment-based configuration for staging and production
- [ ] Add uptime monitoring and deployment notifications

---

## Author

**Muhammad Sajid**, Senior Software Engineer

[LinkedIn](https://linkedin.com/in/mr-sajid) · [GitHub](https://github.com/mrsajiddev)

---

## License

This project is licensed under the [MIT License](LICENSE).