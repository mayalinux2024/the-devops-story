# Container — Opening the Lunchbox (Chapter 7)

## Objective

Understand that a Container is a running instance of a Docker Image.

---

## 🔘 Show the Real Implementation

Run:

```bash
docker run -p 5000:5000 devops-story
```

Open:

```
http://localhost:5000
```

Expected output:

```
📦 Docker Magic Lunchbox

Welcome to the DevOps Story!
```

That's it.

The Docker Image became a running Container.

---

## What Did We Learn?

Docker Image

↓

docker run

↓

Running Container

---

## 📸 Screenshots

- `docker run -p 5000:5000 devops-story`

  <img width="637" height="99" alt="docker-run" src="https://github.com/user-attachments/assets/3d59f391-6ced-48df-b8db-fc8fc4ffe0ed" />

- Browser showing the application.

  <img width="194" height="83" alt="browser-docker-magic-lunchbox-image" src="https://github.com/user-attachments/assets/67ddaa8a-4056-45aa-8a16-0403fbe9a6d8" />

