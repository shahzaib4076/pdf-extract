# PDFExtract

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat&logo=angular)](https://angular.io/)

**PDFExtract** is a world-class, high-performance web utility designed to extract all embedded images from PDF documents in seconds. Built with a focus on privacy and efficiency, it processes files entirely in-memory, ensuring your data never touches the disk.

## ✨ Features

- **🚀 Lightning Fast**: Extract hundreds of images in milliseconds.
- **🛡️ Privacy First**: In-memory processing; no file storage on server.
- **💎 Glassmorphism UI**: Modern, macOS-inspired aesthetic with dark mode.
- **📦 ZIP Export**: All extracted images are bundled into a single ZIP file.
- **⚡ Reactive**: Built with Angular Signals for a seamless user experience.

## 🛠️ Tech Stack

- **Backend**: Python, FastAPI, PyMuPDF (fitz)
- **Frontend**: Angular 19+, Tailwind CSS 4
- **DevOps**: Docker, GitHub Actions

## 🚀 Getting Started

### Prerequisites

- **Standard**: Python 3.9+ and Node.js 18+ & npm
- **Docker**: Docker Engine 20.10+ and Docker Compose v2+

---

### 🐳 Docker Setup (Recommended)

The easiest way to run the full stack locally — no Python or Node.js installation required.

1. **Clone the repository**:
   ```bash
   git clone https://github.com/shahzaibali4076/pdf-extract.git
   cd pdf-extract
   ```

2. **Build and start both services**:
   ```bash
   docker compose up --build
   ```
   Docker will build the backend (FastAPI) and frontend (Angular → Nginx) images, then start them together.

3. **Open the app**:
   Navigate to **[http://localhost:4200](http://localhost:4200)** in your browser.

   | Service  | URL                          |
   |----------|------------------------------|
   | Frontend | http://localhost:4200        |
   | Backend  | http://localhost:8000        |
   | API Docs | http://localhost:8000/docs   |

4. **Stop the services**:
   ```bash
   docker compose down
   ```

> **How it works**: The Angular app is compiled with the backend URL baked in at build time (`NG_APP_API_URL=http://localhost:8000/api`). The frontend container waits for the backend to pass its health check before starting, so the app is always ready on first load.

> **Custom backend URL**: If you need to point the frontend at a different backend (e.g., a remote server), pass the URL as a build argument:
> ```bash
> docker compose build --build-arg NG_APP_API_URL=https://your-backend.example.com/api
> docker compose up
> ```

---

### ⚙️ Standard Setup (Without Docker)

1. **Clone the repository**:
   ```bash
   git clone https://github.com/shahzaibali4076/pdf-extract.git
   cd pdf-extract
   ```

2. **Run the automation script**:
   We provide a convenient `run.py` script that handles dependency installation and starts both servers:
   ```bash
   python backend/run.py
   ```
   *This will automatically open `http://localhost:4200` once ready.*

---

## 🏗️ Architecture

- **Backend**: A RESTful API built with FastAPI that performs low-level PDF parsing using PyMuPDF.
- **Frontend**: A standalone Angular application using SCSS for premium styling and Signals for state management.

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---
*Created and completed from start to finish with ❤️ by [Muhammad Shahzaib Ali](https://github.com/shahzaib4076).*
