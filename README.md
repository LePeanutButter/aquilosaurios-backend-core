# Anquilosaurios - Backend Core

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

> Backend Core for a social, multiplayer web game targeting the Latin American market.

This repository contains the backend service for a multiplayer web application built with ASP.NET Core. It provides the business logic, RESTful API endpoints, and database connectivity required to support user authentication, lobby management, data persistence, and analytics.

---

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [API](#api)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Tools](#tools)
- [Contributing](#contributing)
- [Maintainers](#maintainers)
- [License](#license)

---

## Background

The project addresses the lack of accessible, free, browser-based games optimized for low-end devices and unstable internet connections—common in parts of Latin America. This backend service powers essential multiplayer game features and lays the foundation for future cross-platform expansion (mobile/console).

---

## Install

> Requirements:
> - [.NET 6+ SDK](https://dotnet.microsoft.com/)
> - [Git](https://git-scm.com/)
> - Optional: Azure CLI for deployment

Clone the repository and restore dependencies:

```bash
git clone https://github.com/your-org/multiplayer-webgame-backend.git
cd multiplayer-webgame-backend
dotnet restore
```

To run the backend locally:

```bash
dotnet run
```


The API will be available at **`https://localhost:5001`** (or configured port).

## Usage

This backend is meant to serve:

- Player data logging and analytics
- Feedback collection

- It works together with the Unity WebGL frontend, communicating over a REST API (future versions may incorporate WebSockets or SignalR for real-time communication).

## API

Full API documentation is in progress and will be published via **Swagger**.

**Key endpoints**:

| Method | Endpoint               | Description                                 |
|--------|------------------------|---------------------------------------------|
| POST   | `/auth/login`          | Authenticate player and issue JWT token     |
| POST   | `/auth/register`       | Register a new player account               |
| GET    | `/lobby/list`          | Retrieve available game lobbies             |
| POST   | `/lobby/create`        | Create a new game lobby                     |
| POST   | `/lobby/join`          | Join an existing lobby                      |
| POST   | `/game/start`          | Start the game session                      |
| POST   | `/game/state/update`   | Update game state during session            |
| GET    | `/leaderboard/global`  | Fetch global leaderboard rankings           |
| POST   | `/player/stats`        | Submit player performance stats             |

## Architecture

- **Frontend:** Blazor
- **Game Client:** Unity WebGL
- **Backend:** ASP.NET Core REST API
- **Database:** Azure SQL + MongoDB
- **Deployment:** Azure App Services
- **Security:** HTTPS, JWT tokens for session auth
- **Tools:** GitHub, Azure DevOps, Miro, Figma

Architecture diagrams and business flows are maintained in **Miro** (link available on request). UI mockups and prototypes are created using **Figma**.

## Tech Stack

- **Language:** C#
- **Framework:** ASP.NET Core
- **Database:** Planned - Azure SQL + MongoDB
- **Auth:** JWT (planned)
- **CI/CD:** Azure DevOps Pipelines
- **Cloud:** Azure App Services (planned)
- **Monitoring:** To be defined (App Insights / others)

## Tools

| Tool         | Purpose                                      |
|--------------|----------------------------------------------|
| Figma        | Frontend UI/UX design                        |
| Miro         | Business logic and architecture diagrams     |
| Azure        | Cloud deployment and storage                 |
| GitHub       | Version control and collaboration            |
| Azure DevOps | CI/CD pipelines and project tracking         |

## Contributing

We welcome contributions from developers familiar with **.NET**, **Azure**, or **backend design**. To contribute:

1. Fork the repository

2. Create a new branch:

```bash
git checkout -b feature/my-feature
```

3. Commit your changes:

```bash
git commit -am 'Add new feature'
```

4. Push to the branch:

```bash
git push origin feature/my-feature
```

5. Open a Pull Request

Please make sure to follow coding best practices and write **unit tests** for your changes.

## Maintainers

- [Lanapequin](https://github.com/Lanapequin) - Laura Natalia Perilla Quintero
- [LePeanutButter](https://github.com/LePeanutButter) - Santiago Botero Garcia
- [shiro](https://github.com/JoseDavidCastillo) - Jose David Castillo Rodriguez

## License

MIT

This README follows the <u>**Standard Readme**</u> specification.