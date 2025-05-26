# 💬 Spring Boot WebSocket Chat Application

## 🌟 Overview
A modern **real-time chat application** built with **Spring Boot** and **WebSocket** for instant messaging, integrated with **MySQL** for data persistence and **Js** for a dynamic frontend. This app enables users to join chat rooms, send messages, and receive real-time updates, providing a seamless communication experience. 🚀

## ✨ Key Features
- 💬 **Real-Time Messaging**: Send and receive messages instantly via WebSocket.
- 👥 **User Management**: Register and authenticate users with Spring Security.
- 📚 **Chat Rooms**: Create and join multiple chat rooms for group conversations.
- 🗄️ **Message Persistence**: Store chat history in MySQL for retrieval.
- 🔍 **Search Messages**: Search past messages by keyword or user.
- 📱 **Responsive UI**: React-based frontend for desktop and mobile compatibility.
- 🔒 **Secure Authentication**: JWT-based login for secure access.

## 🛠️ Prerequisites
- ☕ **Java 17** or later
- 📦 **Maven** for dependency management
- 🌐 **Node.js** and **npm** for the React frontend
- 🗄️ **MySQL 5.7** or later
- 🌍 **Modern browser** (Chrome, Firefox, Edge)

## 🚀 Installation

### Backend (Spring Boot)
1. **Clone the Repository** 📂
   ```bash
   git clone https://github.com/yourusername/springboot-websocket-chat.git
   cd springboot-websocket-chat/backend
   ```

2. **Configure Database** 🗄️
   - Create a MySQL database named `chat_db`.
   - Update `src/main/resources/application.properties`:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/chat_db
     spring.datasource.username=your_username
     spring.datasource.password=your_password
     spring.jpa.hibernate.ddl-auto=update
     spring.security.jwt.secret=your_jwt_secret_key
     ```

3. **Build and Run** 🏃
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```
   - Backend runs on `http://localhost:8080`.

### Frontend 
1. **Navigate to Frontend** 📂
   ```bash
   cd ../frontend
   ```

2. **Install Dependencies** 📦
   ```bash
   npm install
   ```

3. **Start Frontend** 🌐
   ```bash
   npm start
   ```
   - Frontend runs on `http://localhost:3000`.

## 🎮 Usage
1. **Access the App** 🌐
   - Open `http://localhost:3000`.
   - Register or log in with credentials 🔐.

2. **Start Chatting** 💬
   - Join or create a chat room from the dashboard.
   - Send messages and see real-time updates via WebSocket.
   - Search chat history by keyword or user.

3. **Key API Endpoints** 📡
   - **User Registration**: `POST /api/auth/register`
     ```json
     {
       "username": "user1",
       "password": "pass123"
     }
     ```
   - **Join Room**: `POST /api/rooms/join`
     ```json
     {
       "userId": 1,
       "roomId": "room1"
     }
     ```
   - **Send Message**: WebSocket endpoint `/ws/chat`
     ```json
     {
       "roomId": "room1",
       "userId": 1,
       "message": "Hello!"
     }
     ```
   - **Health Check**: `GET /actuator/health`

## 📂 Project Structure
```
springboot-websocket-chat/
├── backend/                    # Spring Boot backend 🖥️
│   ├── src/main/
│   │   ├── java/com/example/chat/
│   │   │   ├── controller/     # REST and WebSocket controllers ⚙️
│   │   │   ├── service/        # Business logic 🛠️
│   │   │   ├── model/          # Entities (User, Message, Room) 📋
│   │   │   ├── config/         # WebSocket and Security config 🔧
│   │   ├── resources/
│   │   │   ├── application.properties  # Configuration ⚙️
│   ├── pom.xml                 # Maven dependencies 📦
├── frontend/                   # React frontend 🌐
│   ├── src/
│   │   ├── components/         # React components 🧩
│   │   ├── App.js              # Main React app 🚀
│   ├── package.json            # Node dependencies 📦
├── README.md                   # This file 📄
```

## 🤝 Contributing
Contributions are welcome! To contribute:
1. 🍴 Fork the repository.
2. 🌿 Create a branch: `git checkout -b feature/your-feature`.
3. ✍️ Commit changes: `git commit -m "Add your feature"`.
4. 🚀 Push branch: `git push origin feature/your-feature`.
5. 📬 Open a pull request.

---

🌍 Connect instantly with real-time chat! Happy coding! 🚀
