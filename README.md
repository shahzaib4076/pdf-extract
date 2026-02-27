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

- Python 3.9+
- Node.js 18+ & npm
- Docker (optional, for containerized run)

### Standard Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/pdf-extract.git
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
*Made with ❤️ by a World-Class Full-Stack Developer.*
