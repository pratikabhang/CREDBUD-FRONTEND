# 💳 CREDBUD Frontend

> A React-based web application delivering CREDBUD's interactive user interface, data visualization, API integration, and productivity-focused frontend components.

![React](https://img.shields.io/badge/React-17.0.2-61DAFB?logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?logo=javascript&logoColor=black)
![Chakra UI](https://img.shields.io/badge/Chakra%20UI-1.8.8-319795?logo=chakraui&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-10.14.1-FFCA28?logo=firebase&logoColor=black)
![Create React App](https://img.shields.io/badge/Create%20React%20App-5.0.0-09D3AC?logo=createreactapp&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

## 📖 Overview

**CREDBUD Frontend** is the client-side application for the CREDBUD platform. Built with React and Create React App, it uses Chakra UI and a collection of JavaScript libraries to support interactive user interfaces and data-driven features.

The project includes dependencies for API communication, Firebase integration, charts, QR and barcode scanning, calendars, spreadsheet processing, client-side routing, and animations.

The frontend is maintained independently from the backend API server.

**Related repositories**

- Frontend application: [CREDBUD-FRONTEND](https://github.com/pratikabhang/CREDBUD-FRONTEND)
- Backend API: [CREDBUD-BACKEND-API-Server](https://github.com/pratikabhang/CREDBUD-BACKEND-API-Server)

## ✨ Features

- **Reusable React Components:** Supports modular UI development.
- **UI Components and Theming:** Chakra UI provides reusable interface elements and styling utilities.
- **API Integration:** Axios supports HTTP requests to configured backend services.
- **Firebase Integration:** Includes the Firebase client SDK for configured Firebase functionality.
- **Data Visualization:** ApexCharts and Chart.js-related libraries support chart interfaces.
- **QR and Barcode Scanning:** Includes libraries for scanning workflows.
- **Calendar Interfaces:** React Calendar supports date-based UI components.
- **Spreadsheet Processing:** SheetJS (`xlsx`) supports spreadsheet data processing.
- **Client-Side Navigation:** React Router DOM supports frontend routing.
- **Animations and Icons:** Framer Motion and React Icons support interface presentation.

These are capabilities supported by the dependency set. The exact features available to users depend on the implementation in `src/`.

## 🛠️ Tech Stack

| Technology | Version / Specification | Purpose |
|---|---|---|
| React | 17.0.2 | Frontend framework |
| JavaScript | ES6+ | Application logic |
| Create React App | 5.0.0 | Development and build tooling |
| Chakra UI | 1.8.8 | UI components and styling |
| Firebase | 10.14.1 | Client-side Firebase integration |
| Axios | 1.6.7 | HTTP requests |
| React Router DOM | 5.3.x | Client-side navigation |
| ApexCharts | 3.35.2 | Interactive charts |
| React Chart.js 2 | 5.2.x | Chart.js integration |
| Framer Motion | 4.1.x | UI animations |
| HTML5 QR Code | 2.3.x | QR scanning |
| SheetJS (`xlsx`) | 0.18.x | Spreadsheet processing |
| React Calendar | 3.7.x | Calendar UI |
| React Icons | 4.3.x | Icons |

Check `package.json` and the lockfile for the exact resolved dependency versions.

## 🏗️ Architecture

```text
                    User
                     |
                     v
               React Interface
                     |
            +--------+--------+
            |                 |
            v                 v
       UI Components      React Router
            |                 |
            +--------+--------+
                     |
                     v
              Application Logic
                     |
          +----------+----------+
          |          |          |
          v          v          v
        Axios     Firebase   UI Libraries
          |
          v
    CREDBUD Backend API
    Separate Repository
```

### Main Components

| Component | Responsibility |
|---|---|
| React | Component rendering and frontend state |
| Chakra UI | Layout, styling, and UI components |
| React Router DOM | Client-side navigation |
| Axios | Backend API communication |
| Firebase SDK | Configured Firebase integration |
| Chart libraries | Data visualization |
| QR scanning libraries | Scanning interfaces |
| SheetJS | Spreadsheet processing |
| Framer Motion | Animations |

The backend's request handling, server-side business logic, and authorization are maintained in the separate backend repository.

## 🎯 Scope and Objectives

### In scope

- Build and maintain the CREDBUD user interface.
- Develop reusable React components.
- Support client-side navigation.
- Integrate with configured APIs and external services.
- Present structured data and visualizations.
- Maintain a reproducible frontend development workflow.

### Out of scope

- Backend API implementation.
- Server-side authorization and business logic.
- Backend database administration.
- Production server credentials and infrastructure.
- Backend deployment configuration.

## 📂 Project Structure

```text
CREDBUD-FRONTEND/
├── .netlify/
├── public/
├── src/
├── .env
├── .gitignore
├── .gitattributes
├── CHANGELOG.md
├── LICENSE
├── README.md
├── cert.pem
├── key.pem
├── jsconfig.json
└── package.json
```

- `src/` — React application source.
- `public/` — Static assets.
- `package.json` — Dependencies and npm scripts.
- `CHANGELOG.md` — Project change history.
- `LICENSE` — License information.
- `.netlify/` — Netlify-related configuration.

## 💻 Prerequisites

Install:

- [Node.js](https://nodejs.org/)
- npm
- [Git](https://git-scm.com/)
- A modern web browser

Verify the installed tools:

```bash
node --version
npm --version
git --version
```

Use a Node.js version compatible with the dependencies in the repository.

## 🚀 Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/pratikabhang/CREDBUD-FRONTEND.git
cd CREDBUD-FRONTEND
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Inspect the source code to determine which environment variables are required.

For example, if the application expects a configurable backend API URL:

```env
REACT_APP_API_URL=http://localhost:3000
```

`REACT_APP_API_URL` is an example only. Use the actual variable name expected by the application.

**Security:** Create React App embeds frontend environment variables in the browser bundle. Never place private credentials or server-side secrets in frontend environment variables.

### 4. Configure development HTTPS

The current startup configuration references `cert.pem` and `key.pem`. If HTTPS is required, configure valid local development certificates at the paths expected by the application.

Do not use a real production private key in the development repository.

### 5. Start the development server

```bash
npm start
```

Open the URL shown in the terminal. The existing configuration uses HTTPS and typically serves the application at:

[https://localhost:3000](https://localhost:3000)

The actual URL depends on the development-server configuration and certificate setup.

### 6. Create a production build

```bash
npm run build
```

Create React App generates an optimized production bundle in `build/`.

### 7. Run tests

```bash
npm test
```

This runs the configured test runner. The available test coverage depends on the tests included in the repository.

## ▶️ Usage

1. Clone the frontend repository.
2. Install dependencies.
3. Configure the environment variables required by the application.
4. Start the development server.
5. Open the local application URL in your browser.
6. Use the implemented interface and available frontend features.
7. Verify API-dependent functionality against the configured backend.

### Connecting to the Backend

The backend API is maintained separately:

**[CREDBUD-BACKEND-API-Server](https://github.com/pratikabhang/CREDBUD-BACKEND-API-Server)**

For local full-stack development:

1. Set up and start the backend using its own README.
2. Configure the frontend with the correct API base URL.
3. Ensure backend CORS settings allow the frontend origin.
4. Verify that required API routes and authentication mechanisms are available.
5. Test the frontend's API-dependent features.

The frontend and backend are separate projects and may use different ports or hosting environments.

## ⚙️ Available Scripts

| Command | Purpose |
|---|---|
| `npm start` | Starts the development server |
| `npm run build` | Creates the production build |
| `npm test` | Runs the configured test runner |
| `npm run eject` | Exposes Create React App configuration |
| `npm run predeploy` | Builds the application before deployment |
| `npm run deploy` | Runs the configured GitHub Pages deployment workflow |
| `npm run sitemap` | Executes the configured sitemap script |

Check `package.json` before running deployment commands, because they depend on the configured hosting workflow and supporting packages.

## 🔐 Security Considerations

- Remove exposed credentials from `.env` and rotate affected secrets.
- Never commit real production private keys.
- Apply appropriate Firebase security rules.
- Enforce authentication and authorization on the backend.
- Configure CORS on the backend for trusted origins.
- Review third-party dependencies and security advisories.
- Use properly managed HTTPS certificates in production.
- Validate untrusted input and spreadsheet data before processing.

## 🔮 Future Improvements

- Add component and integration tests.
- Document pages, navigation, and application workflows.
- Provide a sanitized `.env.example`.
- Document API integration and error handling.
- Improve accessibility and responsive design.
- Review legacy dependencies and upgrade them carefully.
- Add CI checks for builds and tests.
- Document the intended frontend deployment platform.
- Remove unused dependencies and development-only configuration.

These are proposed enhancements, not claims about existing functionality.

## 🤝 Contributing

1. Fork the repository.
2. Clone your fork:

   ```bash
   git clone https://github.com/<your-username>/CREDBUD-FRONTEND.git
   cd CREDBUD-FRONTEND
   ```

3. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

4. Make and test your changes.
5. Verify the production build:

   ```bash
   npm run build
   ```

6. Commit your changes:

   ```bash
   git add .
   git commit -m "Improve frontend functionality"
   ```

7. Push your branch:

   ```bash
   git push origin feature/your-feature-name
   ```

8. Open a pull request describing the changes and tests performed.

Never include production credentials, private keys, or sensitive environment files in contributions.

## 📄 License

This repository includes an **MIT License**. Review the checked-in `LICENSE` file for the applicable copyright notice and terms. Preserve the relevant notices and comply with third-party license requirements when redistributing code or assets.

## 👨‍💻 Author

**Pratik Abhang**

- GitHub: [@pratikabhang](https://github.com/pratikabhang)
- Frontend: [CREDBUD-FRONTEND](https://github.com/pratikabhang/CREDBUD-FRONTEND)
- Backend API: [CREDBUD-BACKEND-API-Server](https://github.com/pratikabhang/CREDBUD-BACKEND-API-Server)

---

⭐ If you find this project useful, consider starring the repository.

*Build intuitive interfaces. Visualize data. Deliver better user experiences.*
