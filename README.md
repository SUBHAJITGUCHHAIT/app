# 💬 Real-Time Chat Application

### Spring Boot + WebSocket + STOMP + SockJS

A real-time chat application built using **Spring Boot WebSocket messaging with STOMP protocol**.
This project demonstrates bidirectional communication between clients using a publish–subscribe model.

---

## 🚀 Features

* Real-time messaging (no page refresh)
* WebSocket + STOMP protocol integration
* SockJS fallback support
* Broadcast messaging
* Responsive UI (Bootstrap 5)
* Mobile and Desktop compatible
* Enter key to send message
* Clean chat bubble interface

---

## 🛠 Tech Stack

**Backend**

* Java
* Spring Boot
* Spring WebSocket
* STOMP Messaging
* Maven

**Frontend**

* HTML5
* Bootstrap 5
* JavaScript
* SockJS Client
* STOMP.js

---

## 🧠 Architecture Overview


Client  →  /app/sendMessage   →  @MessageMapping
Server  →  /topic/messages    →  Subscribed Clients


### WebSocket Flow

1. Client connects to `/chat`
2. Client subscribes to `/topic/messages`
3. Client sends message to `/app/sendMessage`
4. Server broadcasts message to all subscribers

## 📂 Project Structure


src/
 ├── main/
 │    ├── java/com/chat/app/
 │    │     ├── config/
 │    │     │     └── WebSocketConfig.java
 │    │     ├── controller/
 │    │     │     └── ChatController.java
 │    │     └── model/
 │    │           └── ChatMessage.java
 │    └── resources/
 │          ├── templates/
 │          │     └── chat.html
 │          └── application.properties



## ⚙️ Configuration

### WebSocket Endpoint

java
registry.addEndpoint("/chat")
        .setAllowedOriginPatterns("*")
        .withSockJS();


### Message Broker

java
registry.setApplicationDestinationPrefixes("/app");
registry.enableSimpleBroker("/topic");


---

## ▶️ How to Run

### 1️⃣ Clone the Repository


git clone https://github.com/your-username/your-repo-name.git


### 2️⃣ Open in IntelliJ IDEA

Open as a Maven project.

### 3️⃣ Run Spring Boot Application

Run the main class:


ChatApplication.java


### 4️⃣ Access in Browser

Desktop:


http://localhost:8080/chat

Mobile (same WiFi):

http://YOUR_LOCAL_IP:8080/chat

---

## 📱 Responsive Design

* Desktop: Centered card layout
* Mobile: Full-screen chat experience
* Scrollable message area
* Sticky input section

---

## 🔐 Future Enhancements

* User authentication (Spring Security)
* Private one-to-one messaging
* Message persistence (MySQL)
* Online user tracking
* Typing indicator
* Dark mode
* Deployment (Render / AWS / Railway)
* Scalable broker (RabbitMQ / Kafka)

---

## 🎯 Learning Outcomes

This project demonstrates:

* Real-time communication architecture
* WebSocket protocol fundamentals
* STOMP messaging model
* Publish–Subscribe design pattern
* Frontend–Backend event-driven integration

---

## 👨‍💻 Author

Subhajit Guchhait

Backend Developer | Java | Spring Boot 

---

## 📌 License

This project is for educational and portfolio purposes.

---

If you find this project useful, consider giving it a ⭐ on GitHub.
