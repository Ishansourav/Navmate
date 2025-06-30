# 🤝 Contributing to NavMate

Thank you for considering contributing to **NavMate – WhatsApp Navigation Chatbot**!  
This is a backend-only project built with **Java**, **Spring Boot**, **Firebase**, and **Render**.

---

## 🚀 Project Overview

NavMate is a backend chatbot system integrated with the **WhatsApp Cloud API**.  
It processes user messages, manages sessions via **Firebase Firestore**, and is deployed using **Render.com** with CI/CD.

> 📌 Focus: Backend logic, API/webhook integration, Firebase session handling, and modular message processing.

---

## 🛠 Tech Stack

- **Java 17+**
- **Spring Boot 3.x**
- **Firebase Admin SDK**
- **WhatsApp Business Cloud API**
- **Maven**
- **Render (deployment)**
- **JUnit + Mockito (testing)**

---

## 📂 Repo Structure (Backend-Focused)

```plaintext
src/
├── controller/         # Webhook controller
├── service/            # Message processing logic
├── model/              # DTOs and POJOs
├── config/             # Firebase & app configuration
├── utils/              # Helper classes
└── test/               # JUnit & Mockito tests
