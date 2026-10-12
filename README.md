# Automation: Express.js with CI/CD to Vercel

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-B4CA65?style=for-the-badge&logo=ejs&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

A simple Express.js application that shows how to deploy a Node.js project to **Vercel** automatically, using **GitHub Actions** for CI/CD.

**[🌐 View Live Demo](https://automation-red-three.vercel.app/)**

---

## 📌 Overview

This repository is a hands-on project focused on building, organizing and deploying web applications with modern development workflows.

The first project, **`01-simple-blog`**, is an Express.js application that renders pages with EJS templates and serves static assets. Every change pushed to `main` is deployed to production automatically, with no manual steps.

---

## ✨ Features

- **Express.js**: a lightweight Node.js web framework
- **EJS templates**: render dynamic HTML pages on the server
- **Static assets**: serve CSS, JavaScript and other public files
- **GitHub Actions**: automated deployment workflow
- **Vercel hosting**: fast, reliable production deployments
- **Secure secrets**: deployment credentials are stored in GitHub Secrets, never in code

---

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

---

## 📂 Project Structure

```text
automation/
├── .github/
│   └── workflows/
│       └── deploy.yml        # CI/CD pipeline
├── 01-simple-blog/
│   ├── index.js              # Express server entry point
│   ├── package.json
│   ├── package-lock.json
│   ├── views/
│   │   └── home.ejs          # EJS template
│   └── public/
│       └── style.css         # Static assets
├── screenshots/
│   └── home-page.png
├── project.json
├── README.md
└── LICENSE
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or later)
- [Git](https://git-scm.com/)

### 1. Clone the repository

```bash
git clone https://github.com/mrsajiddev/automation.git
```

### 2. Go to the application folder

```bash
cd automation/01-simple-blog
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the application

```bash
npm start
```

Then open **[http://localhost:3000](http://localhost:3000)** in your browser.

---

## ⚙️ CI/CD Workflow

Deployment to Vercel is fully automated with GitHub Actions.

### How it works

```text
git push ──▶ GitHub ──▶ GitHub Actions ──▶ Vercel CLI ──▶ 🚀 Live on Vercel
```

1. Make changes to the application.
2. Commit and push the changes to the `main` branch.
3. GitHub Actions detects changes in the app or the workflow file.
4. The workflow installs the Vercel CLI and deploys the project.
5. Vercel builds and hosts the application.

### Workflow file

```text
.github/workflows/deploy.yml
```

The workflow runs when changes are pushed to `main` in either of these paths:

- `01-simple-blog/`
- `.github/workflows/deploy.yml`

It can also be started manually from the **Actions** tab on GitHub.

---

## 🔐 Deployment Configuration

To set up automated deployment, create a Vercel project, then add these secrets under:

**GitHub → Repository → Settings → Secrets and variables → Actions**

| Secret              | Description               |
| ------------------- | ------------------------- |
| `VERCEL_TOKEN`      | Vercel access token       |
| `VERCEL_ORG_ID`     | Vercel team or account ID |
| `VERCEL_PROJECT_ID` | Vercel project ID         |

In your Vercel project settings, set the **Root Directory** to:

```text
01-simple-blog
```

> [!IMPORTANT]
> Always keep credentials in GitHub Secrets. Never commit access tokens or private keys to the repository.

---

## 🖼️ Screenshots

![Home page of the simple blog](screenshots/home-page.png)

---

## 📚 What This Project Covers

- Building Node.js applications with Express.js
- Server-side rendering with EJS
- Git and GitHub workflows
- CI/CD pipelines with GitHub Actions
- Automated production deployments
- Cloud hosting on Vercel

---

## 🗺️ Roadmap

- [x] Build a basic Express.js application
- [x] Configure GitHub Actions for deployment
- [x] Deploy the application to Vercel
- [ ] Add more sample projects
- [ ] Add automated testing (Jest + Supertest)
- [ ] Improve deployment checks and error handling

---

## 🤝 Contributing

Suggestions and improvements are welcome.

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-change`
3. Commit your changes: `git commit -m "Add my change"`
4. Push the branch: `git push origin feature/my-change`
5. Open a pull request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👋 About Me

Hi, I'm **Muhammad Sajid**, a Senior Software Engineer from Lahore, Pakistan, with nearly six years of experience building web applications.

I work mainly with **PHP, Laravel and WordPress**, along with **React, Next.js and Node.js** on the full-stack side. I enjoy designing clean APIs, improving application performance and automating deployments, and I'm increasingly focused on bringing **AI into real-world software**, from LLM-powered features to AI-assisted development workflows.

This repository is part of my ongoing practice with modern DevOps and CI/CD.

**Core skills:** PHP · Laravel · WordPress · React · Next.js · Node.js · NestJS · MySQL · PostgreSQL · REST APIs · AWS · Docker · GitHub Actions · AI Integration

### 📫 Connect with me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/mr-sajid)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mrsajiddev)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mr.sajidbwn@gmail.com)

---

<p align="center">⭐ If you found this project useful, consider giving it a star!</p>
