# 🚀 NavMate - WhatsApp Navigation Chatbot Project
<div>
  <img 
    src="https://raw.githubusercontent.com/Ishansourav/Navmate/main/Assets/Logo/navmate-wordmark.png" 
    alt="NavMate Wordmark"
  />
</div>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
</head>
<body>
  <p><em>"NavMate: Your friendly & smart navigation assistant on WhatsApp."</em></p>
  <blockquote>
  <p><em>A Spring Boot-based chatbot integrated with the WhatsApp Cloud API and Firebase Firestore. NavMate enables real-time navigation assistance and smart conversational interaction via WhatsApp, with modular architecture and cloud deployment.</p></em>
  </blockquote>



  <h2>🔍 Description</h2>
  <p>NavMate is a modular, real-time navigation chatbot built in Java using Spring Boot, integrated with the WhatsApp Cloud API and backed by Firebase Firestore. It provides intelligent location assistance directly through WhatsApp chats with secure webhook handling, modular architecture, and cloud-native deployment via Render. Designed for speed, reliability, and extensibility, NavMate enables users to receive turn-by-turn directions, live traffic updates, and location-based queries in a natural conversational format.</p>

  <h2>✨ Features</h2>
  <ul>
    <li>📲 Real-time messaging via WhatsApp Cloud API</li>
    <li>🔐 Secure and modular Spring Boot backend</li>
    <li>🔥 Session management via Firebase Firestore</li>
    <li>☁️ Deployed using Render with auto CI/CD</li>
    <li>🧠 Custom chatbot flow with scalable async processing</li>
    <li>📊 Fully documented architecture, flowcharts & diagrams</li>
  </ul>

  <h2>🧰 Language & Tools</h2>
  <ul>
    <li><strong>Java + Spring Boot</strong> – Backend & APIs</li>
    <li><strong>Firebase Firestore</strong> – Session persistence</li>
    <li><strong>WhatsApp Cloud API</strong> – User interaction</li>
    <li><strong>Render</strong> – Cloud hosting with CI/CD</li>
    <li><strong>JUnit + Mockito</strong> – Unit & integration testing</li>
    <li><strong>Mermaid.js + SVGs</strong> – Architecture visuals</li>
  </ul>

  <h2>📁 Folder Structure (Fully Expanded)</h2>
<pre><code>navmate/
├── .github/                                # 🔁 CI/CD and GitHub workflows
│   └── workflows/
│       ├── render-deploy.yml               # CI/CD: Auto-deploy to Render
│       └── test.yml                        # CI: Run tests on PR/commit
│
├── assets/                                 # 🎨 Visual assets & branding
│   ├── navmate-logo.svg                    # Project logo (SVG)
│   ├── whatsapp-icon.png                   # WhatsApp brand icon
│   ├── flow-diagram.png                    # Chatbot flow diagram (PNG)
│   ├── architecture-diagram.svg            # Full system architecture
│   ├── ui-chat-preview.png                 # UI/UX preview for documentation
│   ├── bot-avatar.png                      # Bot character/avatar
│   └── render-deploy-guide.png             # Render deployment step visual
│
├── docs/                                   # 📚 Technical documentation
│   ├── architecture.md                     # High-level architecture overview
│   ├── setup-guide.md                      # Local + cloud setup instructions
│   ├── chatbot-flow.md                     # Chatbot decision tree & logic
│   ├── api-reference.md                    # REST API & webhook docs
│   ├── firebase-schema.png                 # Visual of Firestore collections
│   └── contributors.md                     # Contributor guide + credits
│
├── public/                                 # 🌐 Optional frontend/static files
│   └── index.html                          # Placeholder or landing file
│
├── resources/                              # ⚙️ Spring Boot & Firebase config
│   ├── application.properties              # Core app configurations
│   ├── firebaseConfig.json                 # 🔐 Firebase Admin SDK (DO NOT COMMIT)
│   ├── messages.properties                 # i18n / chatbot reply templates
│   └── logback.xml                         # Optional: Custom logging config
│
├── src/
│   ├── main/java/com/navmate/
│   │   ├── controller/                     # 🌐 REST Controllers
│   │   │   └── WebhookController.java      # Handles WhatsApp incoming messages
│   │   │
│   │   ├── service/                        # 🔧 Business Logic Layer
│   │   │   ├── NavMateService.java         # Core message processing logic
│   │   │   └── MessageRouter.java          # Optional: Intent/command routing
│   │   │
│   │   ├── model/                          # 📦 Data Models
│   │   │   ├── MessagePayload.java         # DTO for WhatsApp messages
│   │   │   ├── UserSession.java            # POJO for Firebase session data
│   │   │   └── ReplyTemplate.java          # Format for sending replies
│   │   │
│   │   ├── config/                         # 🔐 Configuration Classes
│   │   │   └── FirebaseConfig.java         # Firebase initialization logic
│   │   │
│   │   ├── utils/                          # 🛠 Utility classes
│   │   │   ├── JsonParserUtil.java         # Parse/validate JSON payloads
│   │   │   └── WhatsAppAPIUtil.java        # Encapsulate API interactions
│   │   │
│   │   └── NavMateApplication.java         # 🚀 Spring Boot main class
│   │
│   └── test/java/com/navmate/             # 🧪 Unit & integration tests
│       ├── controller/                     # Controller layer tests
│       │   └── WebhookControllerTest.java
│       ├── service/                        # Business logic tests
│       │   └── NavMateServiceTest.java
│       └── utils/                          # Utility class tests
│           └── JsonParserUtilTest.java
│
├── .gitignore                              # 🚫 Ignore unnecessary files
├── LICENSE                                 # 📜 MIT License
├── pom.xml                                 # 📦 Maven build configuration
├── render.yaml                             # ⚙️ Render deployment script
├── README.md                               # 📘 GitHub project overview
└── CONTRIBUTING.md                         # 🙌 Contribution guide
</code></pre>


  <h2>📌 System Architecture</h2>
  <pre><code>+ WhatsApp User
      ↓
+ WebhookController (Spring Boot)
      ↓
+ NavMateService (process logic)
      ↓
+ Firebase Firestore ↔ Session DB
      ↓
+ WhatsApp Cloud API (send reply)
      ↓
+ Render (hosting with auto-deploy)</code></pre>

  <h2>🔄 Chatbot Flow Diagram</h2>
  <pre><code>📩 WhatsApp Message
   ↓
🌐 Webhook Controller
   ↓
🔧 NavMate Service
   ↓
🧠 Check Session (in Firestore)
   → Yes → Load Data → Generate Reply
   → No  → Create Session → Generate Reply
   ↓
📤 Send via WhatsApp API
</code></pre>

<h2>⚙️ Setup Instructions</h2>
<pre><code>1️⃣ Clone the repository
git clone https://github.com/your-username/navmate.git
cd navmate
<br>
2️⃣ Install Java and Maven
Ensure Java 17+ and Maven are installed
java -version
mvn -v
<br>
3️⃣ Add Firebase Admin SDK config
Save your Firebase service account key as:
src/main/resources/firebaseConfig.json
Never commit this file to GitHub!
<br>
4️⃣ Set environment variables
(For local testing or Render deployment)
export WHATSAPP_TOKEN=your_whatsapp_api_token
export VERIFY_TOKEN=your_webhook_verify_token
export FIREBASE_CONFIG=src/main/resources/firebaseConfig.json
<br>
5️⃣ Build the project using Maven
mvn clean install
<br>
6️⃣ Run the application
mvn spring-boot:run
<br>
7️⃣ Expose to the web using ngrok (for WhatsApp webhook testing)
ngrok http 8080
<br>
Copy the https URL and paste it into the WhatsApp Cloud API webhook settings:
https://developers.facebook.com/apps/YOUR_APP_ID/webhooks/
<br>
8️⃣ Set webhook verify token
Use the same token in both:
- WhatsApp webhook settings
- VERIFY_TOKEN environment variable
</code></pre>

<h3>☁️ Render Deployment</h3>
<ol>
  <li>Push your project to GitHub (with private firebaseConfig.json excluded)</li>
  <li>Login to <a href="https://render.com" target="_blank">Render.com</a> and click "New Web Service"</li>
  <li>Connect your GitHub repo and choose:
    <ul>
      <li>Environment: <code>Java 17</code></li>
      <li>Build Command: <code>./mvnw clean install</code> (or <code>mvn clean install</code>)</li>
      <li>Start Command: <code>java -jar target/navmate-0.0.1-SNAPSHOT.jar</code></li>
    </ul>
  </li>
  <li>Set the following environment variables under "Environment":
    <ul>
      <li><code>WHATSAPP_TOKEN</code> – Your WhatsApp Cloud API token</li>
      <li><code>VERIFY_TOKEN</code> – Webhook verification token</li>
      <li><code>FIREBASE_CONFIG</code> – Path or JSON string of Firebase credentials</li>
    </ul>
  </li>
  <li>Click “Deploy” and wait for the build</li>
  <li>Use the deployed HTTPS endpoint as your WhatsApp webhook</li>
</ol>

<h3>📁 Firebase Setup</h3>
<ol>
  <li>Go to <a href="https://console.firebase.google.com/" target="_blank">Firebase Console</a> and create a new project</li>
  <li>Enable Firestore (in Native mode)</li>
  <li>Go to Project Settings > Service Accounts > Generate Admin SDK Key</li>
  <li>Download the JSON and save as <code>firebaseConfig.json</code> in <code>src/main/resources/</code></li>
</ol>

<h3>🧪 Running Tests</h3>
<pre><code># Run all unit and integration tests
mvn test
</code></pre>


  <h2>🔮 Upcoming Features</h2>
  <ul>
    <li>🤖 GPT/Dialogflow smart conversation engine</li>
    <li>🌍 Support for regional languages</li>
    <li>📈 Admin dashboard for stats, logs & sessions</li>
    <li>🗂️ History logs per user</li>
    <li>🗺️ Integration with third-party GPS APIs</li>
  </ul>

  <h2>🧠 Strategic Recommendations</h2>
  <ul>
    <li>Implement Redis cache for temporary message/session speedup</li>
    <li>Use GitHub Actions for deeper CI/CD automation</li>
    <li>Enable Firestore batch writes for performance</li>
    <li>Monitor via Sentry, Grafana or Firebase Logs</li>
  </ul>

  <h2>🤝 Contributing</h2>
  <ol>
    <li>🍴 Fork the repository</li>
    <li>🔨 Implement the feature/fix</li>
    <li>✅ Write unit + integration tests</li>
    <li>🚀 Submit a pull request</li>
  </ol>
  <h2>🙏 Acknowledgements</h2>
  <ul>
    <li>💬 Meta – WhatsApp Cloud API</li>
    <li>🔥 Firebase by Google</li>
    <li>☁️ Render.com for deployment</li>
    <li>🧠 OpenAI for architecture & system guidance</li>
  </ul>
  <h2>📜 License</h2>
<p>
  This project is licensed under the 
  <a href="http://www.apache.org/licenses/LICENSE-2.0" target="_blank">
    <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="License: Apache 2.0"/>
  </a>
</p>
<blockquote>
  <em>
    Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an 
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  </em>
</blockquote>
<footer><p>© 2025 NavMate Project. All rights reserved.</p></footer>
</body>
</html>
