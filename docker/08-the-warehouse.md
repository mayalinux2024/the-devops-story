# Docker Registry — The Warehouse (Chapter 8)

A Docker Image doesn't have to stay on your own computer.

It can be stored in a Docker Registry (such as Docker Hub), where anyone with permission can download the exact same image.

---

## Objective

Understand that a Docker Registry is a warehouse for Docker Images.

---

## 🔘 Show the Real Implementation

First, log in to Docker Hub.

```bash
docker login
```

Expected output:

```text
Login Succeeded
```

Next, tag your image with your Docker Hub username.

```bash
docker tag devops-story mayalinux/devops-story:latest
```

Now upload the image to Docker Hub.

```bash
docker push mayalinux/devops-story:latest
```

Expected output:

```text
latest: digest: ...
```

Finally, open Docker Hub in your browser and verify that the **devops-story** repository now exists.

---

The master lunchbox is no longer stored only in the wizard's workshop—it is now stored in the kingdom's warehouse, ready for any worker to use.

The wizard has placed the master lunchbox inside the kingdom's warehouse.

Anyone with permission can now download the exact same lunchbox instead of building it again.

---

## Optional

To download the image from the warehouse in the future:

```bash
docker pull mayalinux/devops-story:latest
```

Verify that it exists locally:

```bash
docker images
```

Run it whenever you need:

```bash
docker run -p 5000:5000 mayalinux/devops-story:latest
```

Then open:

```
http://localhost:5000
```

---

## 📸 Screenshots

1. Successful `docker login`
2. `docker tag`

  <img width="755" height="62" alt="docker-login" src="https://github.com/user-attachments/assets/17c5c78f-c008-4a44-b0cc-e19ceeea100a" />

3. Successful `docker push mayalinux/devops-story:latest`

   <img width="699" height="154" alt="docker-push" src="https://github.com/user-attachments/assets/f241a25e-298f-4753-bcec-5478a2f54880" />

5. Docker Hub showing the **devops-story** repository

   <img width="660" height="234" alt="docker-hub" src="https://github.com/user-attachments/assets/95a38e26-28c1-4456-8d91-059724cbecdd" />
