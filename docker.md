docker.md
Below is the **command-line (CLI) method** for **Problem Statement 5**, written so you can **run it exactly as-is** and also **explain it in exam/viva**.

---

## 1. Docker Installation Verification (CLI)

Docker

Open **Command Prompt / PowerShell** and run:

```bash
docker --version
```

Expected output (example):

```
Docker version 26.x.x, build xxxxx
```

✔ Confirms Docker is installed and running

---

## 2. Pull Image from Docker Hub

Docker Hub

```bash
docker pull nginx
```

Expected:

```
Status: Downloaded newer image for nginx
```

---

## 3. List Docker Images

```bash
docker images
```

You should see:

```
REPOSITORY   TAG     IMAGE ID     SIZE
nginx        latest  xxxxxxxx     xxxMB
```

---

## 4. Run Container (Create + Start)

```bash
docker run -d -p 8081:80 --name mynginx nginx
```

**What this does (say in viva):**

* Creates container from image
* Starts container
* Runs in background
* Maps port 8081 → 80

---

## 5. List Running Containers

```bash
docker ps
```

Shows:

```
mynginx   Up   ...
```

---

## 6. Stop Container

```bash
docker stop mynginx
```

---

## 7. List All Containers (Running + Stopped)

```bash
docker ps -a
```

---

## 8. Start Container Again

```bash
docker start mynginx
```

---

## 9. Restart Container

```bash
docker restart mynginx
```

✔ Container lifecycle demonstrated

---

## 10. (Optional) Remove Container & Image

*(Only if examiner asks)*

```bash
docker stop mynginx
docker rm mynginx
docker rmi nginx
```

---

## Docker Lifecycle Summary (Exam-Ready)

| Operation         | Command                     |
| ----------------- | --------------------------- |
| Verify Docker     | `docker --version`          |
| Pull image        | `docker pull nginx`         |
| List images       | `docker images`             |
| Run container     | `docker run`                |
| Stop container    | `docker stop`               |
| Start container   | `docker start`              |
| Restart container | `docker restart`            |
| List containers   | `docker ps`, `docker ps -a` |

---

## One-Line Viva Answer

> “Docker image was pulled from Docker Hub and a container was created. Container lifecycle operations such as run, stop, start, restart, and listing were performed using Docker CLI.”

---

If you get **any error**, paste:

* The exact command
* The full error output

I’ll fix it immediately.
