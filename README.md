# 🔁 Reverse Proxy with Docker (reverse-proxy-docker-project)

I built this project to understand how NGINX works as a reverse proxy when managing multiple apps in a Docker environment. I wanted to simulate how microservices might be structured, and practise routing traffic to different apps running in separate containers under one local domain. 

I wanted to get more comfortable with how services talk to each other in Docker and how traffic is managed with reverse proxies like NGINX. This kind of pattern is common in production, especially in microservices or containerised environments.

---

## ✅ What I Practised

- Containerised two separate Flask apps using Docker
- Gave each app its own Dockerfile and requirements
- Set up an NGINX reverse proxy with a custom `default.conf` file
- Used Docker Compose to manage everything at once
- Routed traffic based on path — e.g. `/app1` and `/app2`
- Confirmed both apps responded through a single NGINX entry point

---

## 🧪 Running It Locally

I ran everything with Docker Compose like this

---

```bash
docker-compose up --build -d
```

Then to test, I visited

http://localhost/app1 → response from App 1

http://localhost/app2 → response from App 2

It was satisfying to see NGINX route both correctly. 

## Output

http://localhost/app1 → Hello from App 1!
http://localhost/app2 → Hello from App 2!



