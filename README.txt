# Automation — Express.js with CI/CD to Vercel


A simple Express.js application demonstrating how to deploy a Node.js project to **Vercel using GitHub Actions and CI/CD automation**.

## 📌 Overview

This repository is a learning project focused on building, organizing, and deploying web applications with modern development workflows.

The first project, `01-simple-blog`, is a simple Express.js application using EJS templates and static assets.

## ✨ Features

- **Express.js** — Lightweight Node.js web framework.
- **EJS Templates** — Render dynamic HTML pages.
- **Static Assets** — Serve CSS, JavaScript, and other public files.
- **GitHub Actions** — Automate deployment workflows.
- **Vercel Hosting** — Deploy the application to production.
- **Environment Secrets** — Store deployment credentials securely in GitHub Actions.

## 🛠️ Tech Stack

| Technology     | Purpose                        |
| -------------- | ------------------------------ |
| Node.js        | JavaScript runtime             |
| Express.js     | Backend web framework          |
| EJS            | Server-side templating         |
| HTML & CSS     | Frontend structure and styling |
| Git & GitHub   | Version control                |
| GitHub Actions | CI/CD automation               |
| Vercel         | Application hosting            |

## 📂 Project Structure

text
automation/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── 01-simple-blog/
│   ├── index.js
│   ├── package.json
│   ├── package-lock.json
│   ├── views/
│   │   └── home.ejs
│   └── public/
│       └── style.css
├── README.md
└── LICENSE


*Note: The structure above shows the expected files. Remove any entries that don't exist in your repository.*

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

- [Node.js](https://nodejs.org/)
- [Git](https://git-scm.com/)
- A GitHub account

### 1. Clone the Repository

bash
git clone https://github.com/mrsajiddev/automation.git


### 2. Navigate to the Application

bash
cd automation/01-simple-blog


### 3. Install Dependencies

bash
npm install


### 4. Start the Application

bash
npm start


Open your browser and visit:

**[http://localhost:3000](http://localhost:3000)**

## ⚙️ CI/CD Workflow

The project uses GitHub Actions to automate production deployment to Vercel.

### Deployment Flow

1. Make changes to the application.
2. Commit and push your changes to the `main` branch.
3. GitHub Actions detects changes to the application or deployment workflow.
4. The workflow installs the Vercel CLI and deploys the project.
5. Vercel builds and hosts the application.

### GitHub Actions Workflow

Workflow file:

text
.github/workflows/deploy.yml


The workflow is configured to run when changes are pushed to `main` that affect:

- `01-simple-blog/`
- `.github/workflows/deploy.yml`

It can also be triggered manually through the GitHub Actions tab.

## 🔐 Deployment Configuration

To configure automated deployment, set up your Vercel project and add the following repository secrets in:

**GitHub → Repository → Settings → Secrets and variables → Actions**

| Secret              | Description               |
| ------------------- | ------------------------- |
| `VERCEL_TOKEN`      | Vercel access token       |
| `VERCEL_ORG_ID`     | Vercel team or account ID |
| `VERCEL_PROJECT_ID` | Vercel project ID         |

Configure the Vercel project's **Root Directory** as:

text
01-simple-blog


Keep credentials in GitHub Secrets. Never commit access tokens or private credentials to your repository.

## 🌐 Live Demo

**Live Application:** [Open the deployed application](https://your-app.vercel.app)

Replace `https://your-app.vercel.app` with your actual Vercel deployment URL.

## 🖼️ Screenshots

Add screenshots of your application to a `screenshots/` folder in the repository.

For example:

text
automation/
├── screenshots/
│   └── home-page.png
└── README.md


Then display them in this section:



*If you haven't added the screenshot file yet, upload it first. Otherwise, GitHub will show a broken image.*

## 📚 What I'm Learning

- Node.js and Express.js application development
- Server-side rendering with EJS
- Git and GitHub workflows
- CI/CD using GitHub Actions
- Automated production deployments
- Cloud deployment with Vercel

## 🗺️ Roadmap

- [x] Create a basic Express.js application
- [x] Configure GitHub Actions for deployment
- [x] Deploy the application to Vercel
- [ ] Add more sample projects
- [ ] Add automated testing
- [ ] Improve deployment checks and error handling

## 🤝 Contributing

Suggestions and improvements are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a pull request.

## 📄 License

This project is intended for learning and experimentation. If you include an MIT license, add a `LICENSE` file containing the appropriate MIT license text.

---

**Built by [Muhammad Sajid](https://github.com/mrsajiddev)**

