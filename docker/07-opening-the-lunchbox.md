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

Take two screenshots:

- `docker run -p 5000:5000 devops-story`
- Browser showing the application.
