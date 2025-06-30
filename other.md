navmate/                                 # 🌍 Backend Project Root
├── .github/                             # 🔁 GitHub Actions: CI/CD & Tests
│   └── workflows/
│       ├── render-deploy.yml            # Auto-deploy to Render
│       └── test.yml                     # Run tests on PR/commit
│
├── assets/                              # 🎨 Visual assets (backend-only relevant)
│   ├── navmate-logo.svg                 # Project logo (SVG)
│   ├── whatsapp-icon.png                # WhatsApp brand icon
│   ├── flow-diagram.png                 # Chatbot flow architecture
│   ├── architecture-diagram.svg         # System architecture (backend-focused)
│   └── render-deploy-guide.png          # Render deployment visual guide
│
├── docs/                                # 📚 Backend Technical Documentation
│   ├── architecture.md                  # Layered backend system breakdown
│   ├── setup-guide.md                   # Backend local + cloud setup
│   ├── chatbot-flow.md                  # Bot logic, command handling
│   ├── api-reference.md                 # Webhook/API endpoint docs
│   ├── firebase-schema.png              # Firestore schema (sessions, messages)
│   └── contributors.md                  # Credits + contribution guidelines
│
├── resources/                           # ⚙️ Spring Boot & Firebase Config
│   ├── application.properties           # Main application config
│   ├── firebaseConfig.json              # 🔐 Firebase Admin SDK (DO NOT COMMIT)
│   ├── messages.properties              # i18n / chatbot replies
│   └── logback.xml                      # Optional custom logging config
│
├── src/
│   ├── main/java/com/navmate/
│   │   ├── controller/                  # 🌐 REST Controller
│   │   │   └── WebhookController.java   # WhatsApp webhook entry point
│   │   │
│   │   ├── service/                     # 🔧 Core Business Logic
│   │   │   ├── NavMateService.java      # Main message handling logic
│   │   │   └── MessageRouter.java       # Optional: command routing
│   │   │
│   │   ├── model/                       # 📦 Data Models / DTOs
│   │   │   ├── MessagePayload.java      # WhatsApp message structure
│   │   │   ├── UserSession.java         # Firebase session structure
│   │   │   └── ReplyTemplate.java       # Bot response formatting
│   │   │
│   │   ├── config/                      # 🔐 Firebase & API Configs
│   │   │   └── FirebaseConfig.java      # Firebase init
│   │   │
│   │   ├── utils/                       # 🛠 Helpers
│   │   │   ├── JsonParserUtil.java      # JSON parsing / validation
│   │   │   └── WhatsAppAPIUtil.java     # Outgoing API abstraction
│   │   │
│   │   └── NavMateApplication.java      # 🚀 Spring Boot entry class
│   │
│   └── test/java/com/navmate/          # 🧪 JUnit + Mockito Tests
│       ├── controller/
│       │   └── WebhookControllerTest.java
│       ├── service/
│       │   └── NavMateServiceTest.java
│       └── utils/
│           └── JsonParserUtilTest.java
│
├── .gitignore                           # 🚫 Git ignore rules
├── LICENSE                              # 📜 MIT License
├── pom.xml                              # 📦 Maven project config
├── render.yaml                          # ☁️ Render deployment config
├── README.md                            # 📘 Project overview (backend-focused)
└── CONTRIBUTING.md                      # 🙌 How to contribute (backend)
