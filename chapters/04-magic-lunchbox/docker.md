# Docker

Docker packages everything an application needs into one portable image.

In Chapter 4 of the story, this is the King's Magic Lunchbox.

Contents:

- app.py
- Dockerfile
- requirements.txt

Build

docker build -t devops-story .

Run

docker run -p 5000:5000 devops-story

Open

http://localhost:5000
