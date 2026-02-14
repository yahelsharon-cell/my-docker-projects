# DevOps Admin Stack: MariaDB & Adminer

A professional multi-container setup demonstrating core Docker principles including orchestration, isolated networking, and data persistence.

## 🚀 Overview
This project deploys a secure MariaDB database alongside Adminer, a web-based database management tool. Instead of manual installation, the entire infrastructure is defined as code using Docker Compose.

## 🛠️ Key DevOps Concepts Applied

* **Infrastructure as Code (IaC):** Used `docker-compose.yml` to define the entire stack, ensuring environment parity.
* **Data Persistence (Volumes):** Implemented a bind mount (`./db_data`) to ensure database records survive container restarts or deletions.
* **Isolated Networking:** Created a private bridge network (`backend_net`) allowing containers to communicate via internal DNS (using service names like `db`) without exposing the database directly to the public internet.
* **Detached Operations:** Configured the stack to run in background mode (`-d`) for production-like behavior.

## Acknowledgments
This project was developed with the assistance of AI tools (Gemini) for troubleshooting and generating documentation.

## 📦 How to Run
1. Ensure you have Docker and Docker Compose installed.
2. Clone this repository.
3. Run the following command:
   ```bash
   docker-compose up -d
