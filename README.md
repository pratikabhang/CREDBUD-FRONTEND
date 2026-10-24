# 💳 CREDBUD — Frontend

> A React-based web dashboard for CREDBUD, built with Chakra UI and modern JavaScript libraries for data visualization, authentication integration, and interactive user interfaces.

![React](https://img.shields.io/badge/React-17.0.2-61DAFB?logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?logo=javascript&logoColor=black)
![Chakra UI](https://img.shields.io/badge/Chakra%20UI-1.8.8-319795?logo=chakraui&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-10.14.1-FFCA28?logo=firebase&logoColor=black)
![Create React App](https://img.shields.io/badge/Create%20React%20App-5.0.0-09D3AC?logo=createreactapp&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

## 📖 Overview

**CREDBUD Frontend** is a React application built with Create React App and Chakra UI. It provides the client-side foundation for the CREDBUD platform, with supporting libraries for API communication, authentication integration, data visualization, QR/barcode scanning, calendar interfaces, and spreadsheet processing.

The application uses reusable UI components and frontend libraries to support interactive dashboard experiences.

This repository contains the frontend codebase. Backend services and API endpoints are maintained separately.

🔗 **Frontend Repository:** [pratikabhang/FRONTEND](https://github.com/pratikabhang/FRONTEND)

🔗 **Related Backend:** [pratikabhang/BACKEND](https://github.com/pratikabhang/BACKEND)

## ✨ Features and Capabilities

The project dependencies provide the following capabilities:

- **Component-Based UI:** React enables reusable components and maintainable interface development.
- **UI Components and Theming:** Chakra UI provides accessible components and styling utilities.
- **API Communication:** Axios supports HTTP requests to backend services.
- **Authentication Integration:** Firebase provides client-side SDK capabilities for supported authentication and application services.
- **Data Visualization:** ApexCharts and Chart.js integrations support interactive charts and graphical representations.
- **QR and Barcode Scanning:** Libraries such as `html5-qrcode`, `instascan`, and `@thewirv/react-barcode-scanner` provide scanning capabilities.
- **Calendar Interfaces:** React Calendar supports date-based UI components.
- **Spreadsheet Processing:** SheetJS (`xlsx`) enables reading and writing spreadsheet data.
- **Routing:** React Router DOM supports client-side navigation.
- **Animations and Icons:** Framer Motion and React Icons support interface animations and iconography.

The availability of a library does not guarantee that every capability is implemented or enabled in the current application.

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|---|---|---|
| React | 17.0.2 | Frontend framework |
| JavaScript | ES6+ | Application logic |
| Create React App | 5.0.0 | Development and build tooling |
| Chakra UI | 1.8.8 | UI components and styling |
| Firebase | 10.14.1 | Client-side Firebase integration |
| Axios | 1.6.7 | HTTP requests |
| React Router DOM | 5.3.x | Client-side routing |
| ApexCharts | 3.35.2 | Interactive charts |
| React Chart.js 2 | 5.2.x | Chart.js integration |
| Framer Motion | 4.1.x | Animations |
| HTML5 QR Code | 2.3.x | QR code scanning |
| SheetJS (`xlsx`) | 0.18.x | Spreadsheet processing |
| React Calendar | 3.7.x | Calendar UI |
| React Icons | 4.3.x | Icon library |

Versions above reflect the declared dependency specifications in `package.json`; ranges using `^` may resolve to later compatible versions.

## 🏗️ Architecture

The frontend follows a component-based React architecture.

```text
                  User
                   |
                   v
              React Interface
                   |
          +--------+---------+
          |                  |
          v                  v
     UI Components       Page Routing
          |                  |
          +--------+---------+
                   |
                   v
          Application Logic
                   |
       +-----------+-----------+
       |           |           |
       v           v           v
     Axios      Firebase    UI Libraries
       |
       v
  Backend REST API
  (Separate Repository)
```

### Architectural Components

| Component | Responsibility |
|---|---|
| React | Component rendering and application state |
| Chakra UI | UI components, layout, and styling |
| React Router | Client-side navigation |
| Axios | Communication with backend APIs |
| Firebase SDK | Integration with configured Firebase services |
| Chart libraries | Data visualization |
| QR scanning libraries | QR and barcode scanning capabilities |
| SheetJS | Spreadsheet data processing |

The exact page hierarchy, state-management approach, and API contracts should be verified against the implementation in `src/`.

## 🎯 Project Objectives

- Provide a modular React frontend for CREDBUD.
- Build interactive interfaces using reusable UI components.
- Integrate frontend functionality with backend services.
- Support data visualization and structured data presentation.
- Provide reusable capabilities for scanning, calendar interfaces, and spreadsheet processing.
- Maintain a development workflow based on npm and Create React App.

## 📂 Project Structure

```text
FRONTEND/
├── .netlify/             # Netlify-related configuration
├── public/               # Static assets
├── src/                  # React application source
├── .env                  # Environment configuration; keep secrets private
├── .gitignore            # Git ignore rules
├── .gitattributes        # Git file-handling configuration
├── CHANGELOG.md          # Project change history
├── LICENSE               # MIT license file
├── cert.pem              # TLS certificate file
├── key.pem               # TLS private key file
├── jsconfig.json         # JavaScript project configuration
└── package.json          # Dependencies and npm scripts
```

The `src/` directory contains the application code, while `public/` contains static assets. The precise component and page organization can be explored directly in the repository.

## 💻 Prerequisites

Install the following tools before starting development:

- **Node.js:** A version compatible with React 17 and the project's dependencies.
- **npm:** Included with Node.js.
- **Git:** For cloning and version control.
- A modern web browser.

Check your installed versions:

```bash
node --version
npm --version
git --version
```

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/pratikabhang/FRONTEND.git
cd FRONTEND
```

### 2. Install Dependencies

```bash
npm install
```

This installs the dependencies defined in `package.json`.

### 3. Configure Environment Variables

Inspect the source code to identify the environment variables required by the application.

Create a local `.env` file with the actual variables expected by the frontend. For example, if the application uses a backend API URL, its configuration could be:

```env
REACT_APP_API_URL=http://localhost:3000
```

This variable name is an example only; confirm the name used by the application before relying on it.

For Create React App, custom frontend environment variables generally need the `REACT_APP_` prefix. Variables embedded into the browser bundle are **not secrets** and must never contain private API credentials or server-side keys.

### 4. Start the Development Server

The `start` script in `package.json` enables HTTPS and references `cert.pem` and `key.pem`.

Run:

```bash
npm start
```

Ensure the required development certificates exist and are configured correctly. The application should open in your browser using the development server URL shown in the terminal, typically:

[https://localhost:3000](https://localhost:3000)

Accept a local certificate warning only when you understand that the certificate is intended for local development. Do not bypass certificate validation for public or production services.

### 5. Create a Production Build

```bash
npm run build
```

Create React App generates an optimized production bundle in the `build/` directory.

### 6. Run Tests

```bash
npm test
```

This invokes the configured Create React App test runner.

## ▶️ Usage

### Running the Frontend Locally

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Configure the required environment variables.
4. Ensure the backend and any required external services are available.
5. Run `npm start`.
6. Open the application URL displayed in the terminal.
7. Explore the available pages and interact with the implemented features.

### Connecting to the Backend

The frontend has a related backend repository:

[**CREDBUD Backend**](https://github.com/pratikabhang/BACKEND)

Before connecting the applications, confirm the backend's configured port, available routes, CORS settings, and required authentication headers. Configure the frontend's API base URL according to the actual Axios configuration.

## 📊 Available npm Scripts

The project's `package.json` defines the following scripts:

| Command | Description |
|---|---|
| `npm start` | Starts the HTTPS development server |
| `npm run build` | Creates a production build |
| `npm test` | Runs the test runner |
| `npm run eject` | Exposes the underlying Create React App configuration |
| `npm run predeploy` | Runs the production build before deployment |
| `npm run deploy` | Deploys the `build/` directory using GitHub Pages tooling |
| `npm run sitemap` | Executes the sitemap-builder script |

**Note:** The deployment scripts require their associated dependencies and configuration. Verify the target hosting platform before using them.

## 🔐 Security Considerations

- **Private keys:** Never commit real TLS private keys. If `key.pem` contains an exposed private key, replace it and review repository history.
- **Environment variables:** Remove exposed credentials from `.env`, rotate affected secrets, and use deployment-specific secret storage.
- **Firebase configuration:** Apply appropriate Firebase security rules and restrictions. Client-side Firebase configuration does not replace server-side authorization.
- **API security:** Validate permissions and sensitive operations on the backend rather than relying on frontend checks.
- **Dependencies:** Review outdated packages and security advisories before production deployment.
- **HTTPS:** Use properly managed certificates in production.
- **User input:** Validate untrusted data before displaying it or processing uploaded spreadsheets.

## 🔮 Future Improvements

Potential improvements include:

- Add component-level and integration tests.
- Document the application's pages and navigation.
- Add a sanitized `.env.example`.
- Document backend API endpoints and request/response formats.
- Improve error handling and loading states.
- Add accessibility and responsive-design checks.
- Upgrade legacy dependencies through a tested migration plan.
- Configure continuous integration for builds and tests.
- Review the QR scanning libraries and remove unused dependencies.
- Document deployment and environment-specific configuration.

These are suggested improvements, not claims about existing functionality.

## 🤝 Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Clone your fork:

   ```bash
   git clone https://github.com/<your-username>/FRONTEND.git
   cd FRONTEND
   ```

3. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

4. Make your changes in the relevant React components or configuration files.
5. Run tests and verify the production build.
6. Commit your changes:

   ```bash
   git add .
   git commit -m "Improve frontend functionality"
   ```

7. Push your branch:

   ```bash
   git push origin feature/your-feature-name
   ```

8. Open a pull request describing your changes and testing performed.

## 📄 License

The repository contains an MIT license file. The checked-in license text identifies **Horizon UI** as the copyright holder for the licensed material.

Review the license and the provenance of the source code before redistributing the project. Ensure that original contributions and third-party assets retain their applicable copyright and licensing notices.

## 👨‍💻 Author

**Pratik Abhang**

- GitHub: [@pratikabhang](https://github.com/pratikabhang)
- Frontend Repository: [FRONTEND](https://github.com/pratikabhang/FRONTEND)
- Related Backend: [BACKEND](https://github.com/pratikabhang/BACKEND)

---

⭐ If you find this project useful, consider starring the repository.

*Build intuitive interfaces. Visualize data. Deliver a better user experience.*
