# Docker - The Magic Lunchbox (Chapter 4)

## Objective

Package an application and everything it needs into one portable package using Docker.

---

# 🔘 Show Me the Real Implementation

↓

# 📄 Implementation Guide

## Implementation Summary

This is the first Docker implementation in the project.

Instead of installing Python and Flask manually on every server, Docker packages everything into one image.

The learner only needs to complete these steps:

Create a simple Flask application

↓

Create a requirements.txt file

↓

Create a Dockerfile

↓

Build the Docker image

↓

Run the Docker container

↓

Open the application in the browser

↓

Verify it works

That's it.

The learner has successfully built the King's Magic Lunchbox.

---

# Detailed Explanation

## Files

### app.py

A simple Flask application.

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "<h1>📦 Docker Magic Lunchbox</h1><p>Welcome to the DevOps Story!</p>"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
```

---

### requirements.txt

```text
Flask==3.1.0
```

---

### Dockerfile

```dockerfile
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["python", "app.py"]
```

---

# Build the Image

```bash
docker build -t devops-story .
```

---

# Verify the Image

```bash
docker images
```

Expected output:

```
devops-story    latest
```

---

# Run the Container

```bash
docker run -p 5000:5000 devops-story
```

---

# Open the Application

Open:

```
http://localhost:5000
```

Expected output:

```
📦 Docker Magic Lunchbox

Welcome to the DevOps Story!
```

---

# Screenshots

- Docker Build

  <img width="842" height="269" alt="docker-build" src="https://github.com/user-attachments/assets/8b728a65-0385-4807-8b95-0fe8b02bb6e0" />

- Docker Images

  <img width="466" height="71" alt="docker-images" src="https://github.com/user-attachments/assets/eedaea4f-dc7b-4649-8f2a-bb2b31a4714d" />

- Running Container

  <img width="637" height="99" alt="docker-run" src="https://github.com/user-attachments/assets/64bae966-a0a2-4e32-8fab-b5f85cdc3532" />

- Browser Output

  <img width="194" height="83" alt="browser-docker-magic-lunchbox-image" src="https://github.com/user-attachments/assets/ff266eaa-9a7f-48bd-b423-98f500425464" />

---

# What Did We Learn?

In the story:

The learner has successfully built the King's Magic Lunchbox.

The lunchbox contains everything a worker needs.

---

# Dockerfile - The lunchbox Blueprint (Chapter 5)

## Objective

Understand that a Dockerfile is simply the recipe used to build a Docker image.

---

## 🔘 Show the Real Implementation

Open the Dockerfile.

```bash
cat Dockerfile
```

Expected output:

```dockerfile
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["python", "app.py"]
```

### What each instruction means

- `FROM` → Start with an existing box.
- `WORKDIR` → Choose where work happens inside the box.
- `COPY` → Put files into the box.
- `RUN` → Install everything the application needs.
- `EXPOSE` → Tell others which door the application uses.
- `CMD` → Tell the worker what to do when the box opens.

That's it.

You have now seen the blueprint the wizard follows to build every identical magic lunchbox.

---

## 📸 Screenshot

- Dockerfile displayed in the terminal using:

```bash
cat Dockerfile

  <img width="479" height="200" alt="Dockerfile" src="https://github.com/user-attachments/assets/63368b2c-02ba-4880-8d91-0b17552c9411" />
