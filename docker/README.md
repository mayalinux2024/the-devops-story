# Docker - The Magic Lunchbox

## Objective

Package an application and everything it needs into one portable Docker image.

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
- Docker Images
- Running Container
- Browser Output

---

# What Did We Learn?

In the story:

📦 Magic Lunchbox

↓

Real World:

🐳 Docker Image

The lunchbox contains everything a worker needs.

A Docker image contains everything an application needs to run anywhere.
