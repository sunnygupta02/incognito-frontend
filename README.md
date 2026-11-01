# IncognitoCampus — Anonymous Real-Time Chat Platform

An anonymous, room-based chat platform for college students built with
React and Spring Boot. Students join campus and branch-specific rooms,
chat in real time over WebSocket, and messages auto-delete after 24 hours.

**Live:** [incognito-campus-frontend.vercel.app](https://incognito-campus-frontend.vercel.app)

---

## Tech stack

| Layer    | Technology                           |
| -------- | ------------------------------------ |
| Frontend | React.js                             |
| Backend  | Spring Boot, Spring MVC, WebSocket   |
| Database | MongoDB                              |
| AI       | Gemini AI API                        |
| Deploy   | Vercel (frontend), Railway (backend) |

---

## Features

- Anonymous usernames — auto-generated at registration, no personal info stored
- Room-based architecture — college and branch-specific chat rooms
- Real-time messaging via WebSocket with sub-100ms latency
- Auto-deleting messages — cleared after 24 hours for privacy
- AI summarization — Gemini API condenses long conversations into digests

---

## Running locally

### Prerequisites

- Node.js 18+
- Java 17+
- MongoDB
- Maven

### Frontend

```bash
cd frontend
npm install
npm start
```

### Backend

```bash
cd backend
mvn clean install
java -jar target/incognito-campus.jar
```

---

## Architecture

- REST APIs handle user, room, and message management
- WebSocket layer manages real-time bidirectional communication
- MongoDB stores room and message data with TTL index for auto-deletion
