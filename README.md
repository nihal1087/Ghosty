# Ghosty 👻

A full-stack Node.js application for sharing and exploring ghostly encounters, built using the native Node HTTP module (no Express) and served as a single same-origin deployment.

The project includes a static frontend, REST APIs, Server-Sent Events (SSE) for live updates, file-based persistence, and an event-driven backend architecture.

---

## ✨ Features

- 🧠 Vanilla Node.js backend (no frameworks)
- 🎨 Static frontend (HTML, CSS, JavaScript)
- 🔁 Server-Sent Events (SSE) for live news updates
- 📦 File-based data storage (JSON)
- 🔔 Event-driven architecture using EventEmitter
- 🧼 Input sanitization for security
- 🌐 Same-origin full-stack deployment (no CORS issues)

---

## 🏗️ Project Architecture

```
from-the-other-side/
│
├── server.js                # HTTP server & routing
├── package.json
├── package-lock.json
│
├── public/                  # Frontend (static files)
│   ├── index.html
│   ├── news.html
│   ├── sightings.html
│   ├── upload-sighting.html
│   ├── index.css
│   ├── index.js
│   └── images/
│
├── handlers/
│   └── routeHandlers.js     # API route handlers
│
├── utils/
│   ├── serveStatic.js
│   ├── getData.js
│   ├── parseJSONBody.js
│   ├── sendResponse.js
│   ├── addNewSighting.js
│   └── sanitizeInput.js
│
├── events/
│   └── sightingEvents.js    # EventEmitter logic
│
├── data/
│   ├── data.json            # Persistent storage
│   └── stories.js           # Live news stories
│
└── test.http                # API testing (VS Code REST Client)

```

---

## 🚀 Live Demo

https://ghosty-l50w.onrender.com
---

## 🔌 API Endpoints

### Get All Sightings
```
GET /api
```
#### Response
```
[
  {
    "title": "Midnight Whisper",
    "location": "Old Hostel",
    "description": "Heard footsteps at 3 AM..."
  }
]
```

### Add a New Sighting
```
POST /api
```
#### Body
```
{
  "title": "Shadow Figure",
  "location": "Library",
  "description": "A dark figure appeared near the stairs."
}
```


### Live News Updates (SSE)
```
GET /api/news
```
- Sends live updates every 3 seconds
- Implemented using Server-Sent Events
- Automatically cleans up connections on client disconnect



---

## 🛠️ Local Setup

```bash
git clone https://github.com/your-username/from-the-other-side.git
cd from-the-other-side
npm install
npm start
```

Open:
```
http://localhost:8000
```

---
## 🧠 Learning Outcomes

- Deep understanding of Node.js internals
- Manual routing and HTTP handling
- Event-driven backend design
- Real-time data streaming (SSE)
- Clean separation of concerns

---


## ☁️ Deployment

- Deployed on Render
- Uses `process.env.PORT`
- Single Node service serving frontend + backend
- SSE supported

---






## 👤 Author

**Nyl**  
Computer Science Student

---

## 📜 License

ISC License
