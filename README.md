# 📞 Talkoo 🎥

**Talkoo** is a full-stack real-time video and chat application built with **Node.js**, **Express**, **React**, and the **Stream Chat API**. It allows users to engage in seamless video conversations and real-time messaging, offering a modern communication experience with a clean and responsive interface.

---

## 🚀 Key Features

- 🔁 Real-time video conferencing
- 💬 Instant messaging powered by Stream Chat API
- 🔐 Secure user authentication and JWT-based authorization
- ⚡ WebSocket-powered real-time communication
- 📱 Responsive and user-friendly React interface
- 🧩 Modular and scalable architecture

---

## 🛠️ Tech Stack

| Layer     | Technology       |
|-----------|------------------|
| Frontend  | React, WebSocket |
| Backend   | Node.js, Express |
| Chat API  | Stream Chat API  |
| Auth      | JSON Web Tokens  |

---

## 🧱 Project Architecture

### 📦 Backend

Built with **Node.js** and **Express**, the backend handles:

- User authentication and JWT generation
- Real-time message routing
- Integration with the Stream Chat API

**Folder structure:**

backend/
├── api/ # API endpoints
├── config/ # App configuration and env
├── controllers/ # Request handlers
├── models/ # Mongoose models
├── routes/ # Express routes
└── utils/ # Helper functions (auth, etc.)

yaml
Kopyala
Düzenle

---

### 💻 Frontend

Built using **React**, the frontend manages:

- UI rendering and state management
- Chat and video interfaces
- API communication with backend

**Folder structure:**

frontend/
├── components/ # Reusable UI components
├── containers/ # Main views and pages
├── actions/ # Redux action creators
├── reducers/ # Redux reducers
└── utils/ # WebSocket and helper utilities

yaml
Kopyala
Düzenle

---

## ⚙️ Getting Started

### 1. 📥 Install Dependencies

```bash
npm install
Run this in both /frontend and /backend directories.

2. 🔙 Run the Backend
bash
Kopyala
Düzenle
cd backend
node server.js
3. 💻 Run the Frontend
bash
Kopyala
Düzenle
cd frontend
npm start
4. 🌐 Environment Variables
Create a .env file in the root of the backend with the following content:

env
Kopyala
Düzenle
STREAM_CHAT_API_KEY=your_stream_key
STREAM_CHAT_API_SECRET=your_stream_secret
JWT_SECRET=your_jwt_secret
PORT=3000
Replace the values with your actual credentials.

📡 API Documentation
🔐 Authentication
Endpoint	Method	Description
/login	POST	Authenticate user, returns JWT
/register	POST	Register new user, returns JWT

💬 Chat
Endpoint	Method	Description
/chat	GET	Fetch all chat channels
/chat	POST	Create a new chat channel
/chat/:channelId	GET	Get specific channel details
/chat/:channelId/message	POST	Send a message to the channel

🔌 Integrating Stream Chat API
Create a StreamChat instance with your API credentials:

javascript
Kopyala
Düzenle
const { StreamChat } = require('stream-chat');

const chat = StreamChat.getInstance('your_api_key', 'your_api_secret');
🧪 Usage Examples
✅ Sending a Message
javascript
Kopyala
Düzenle
chat.sendMessage('channelId', {
  text: 'Hello, world!',
  user: { id: 'userId' }
});
📥 Receiving Messages
javascript
Kopyala
Düzenle
chat.on('message.new', (event) => {
  console.log(event.message.text);
});
🔒 Authentication & Authorization
JWTs are issued upon login or registration.

All protected endpoints validate the JWT in the Authorization header.

Middleware ensures only authenticated users access restricted resources.

🧑‍💻 Development vs Production
Development
bash
Kopyala
Düzenle
npm run dev
Typically runs both frontend and backend concurrently using tools like concurrently.

Production
Build frontend using:

bash
Kopyala
Düzenle
npm run build
Serve frontend with a production-grade server (e.g., NGINX).

Ensure all .env variables are properly configured in deployment environment.

📄 License
This project is not currently licensed. You may add a license of your choice (e.g., MIT, Apache 2.0) depending on your distribution preferences.

🙌 Contributing
Coming soon! (Or add your contribution guidelines here)

📬 Contact
For inquiries, reach out via GitHub Issues or integrate with a contact form if deployed.

