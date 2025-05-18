# 📬 Notification Service

A simple notification service built with **FastAPI**, **RabbitMQ**, and **SQLite**. Supports retry logic for failed notifications and asynchronous processing using a queue.

---

## 🚀 Features

- 📨 Send notifications (Email, SMS, In-App)
- 🐇 Queue-based processing using RabbitMQ
- 🔁 Retry logic for failed notifications
- 🗂️ SQLite for persistence (lightweight, no setup needed)
- 📱 REST API for sending and retrieving notifications

---

## 🧰 Tech Stack

- Python 3.10+
- FastAPI
- SQLite (via SQLAlchemy)
- RabbitMQ
- Pika (RabbitMQ client)
- Uvicorn

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/notification-service.git
cd notification-service


Install Dependencies
py -m pip install fastapi uvicorn sqlalchemy pika httpx



Start RabbitMQ
Make sure RabbitMQ is running locally on default settings (localhost:5672).
You can download RabbitMQ here.

 Initialize the Database
py -c "from models import init_db; init_db()"



Start the FastAPI Server
py -m uvicorn main:app --reload


API will be live at: http://127.0.0.1:8000/docs


Start the Queue Worker
In a new terminal, run:

py queue_worker.py

