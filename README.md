# 🚀 Talkoo Backend

## 📋 Project Title and Description
Talkoo is a **real-time video and chat application** built with Node.js and Express.  
This backend project provides a robust foundation for the application, handling authentication, token generation, and protected routes using middleware.  
It integrates the **Stream Chat API** for seamless chat functionality and user onboarding.

---

## ✨ Features
- 💬 Real-time chat functionality using Stream Chat API  
- 👤 User onboarding and authentication  
- 🔑 Token generation and validation  
- 🔒 Protected routes using middleware  
- ⚙️ Scalable and efficient backend infrastructure  

---

## 🛠️ Technologies Used
- 🟢 Node.js  
- 🚂 Express  
- 💬 Stream Chat API  
- 🔐 Middleware for authentication and authorization  

---

## ⚙️ Installation Instructions

### 🔑 Environment Variables Setup
To run the backend, you'll need to set up the following environment variables:

```env
STREAM_CHAT_API_KEY=your_api_key
STREAM_CHAT_API_SECRET=your_api_secret
JWT_SECRET=your_jwt_secret
PORT=3000
Replace the values with your actual API keys and secrets.

📦 Installing Dependencies
Run the following command to install the required dependencies:

bash
Kopyala
Düzenle
npm install
▶️ Usage Instructions
🚀 Starting the Server
To start the server, run:

bash
Kopyala
Düzenle
npm start
The server will listen on the port specified in the PORT environment variable (default: 3000).

🛣️ Endpoints Overview
Method	Endpoint	Description
POST	/login	Authenticates a user and returns a token
POST	/register	Creates a new user and returns a token
GET	/protected	A protected route that requires a valid token
GET	/chat	Returns a list of chat channels
POST	/chat	Creates a new chat channel

🤝 Contributing Guidelines
Contributions are welcome!
If you'd like to contribute to the Talkoo backend, please fork the repository and submit a pull request with your changes.

📄 License
The Talkoo backend is licensed under the MIT License.

📞 Contact Information or Support
For any questions or issues, please contact us at:
✉️ support@talkoo.com
