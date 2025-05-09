# 🔁 Reverse Proxy with Docker (reverse-proxy-docker-project)

This project sets up two separate Flask apps and routes traffic to them using a single NGINX reverse proxy. It’s built entirely with Docker and Docker Compose to simulate a basic microservices setup where different services are accessible via different URL paths under the same domain.

---

## ✅ What This Project Covers

- Created two minimal Flask apps with individual Dockerfiles
- Set up a reverse proxy using NGINX
- Used `default.conf` to configure NGINX routing rules
- Orchestrated everything using Docker Compose
- Exposed both apps on different paths via `localhost`
- Practised container linking and path-based routing

---

## 🗂️ Project Structure

reverse-proxy-docker-project/
├── app1/
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
├── app2/
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
├── nginx/
│   └── default.conf
└── docker-compose.yml
## 1. Clone and navigate into the project

---

```bash
git clone https://github.com/your-username/reverse-proxy-docker-project.git
cd reverse-proxy-docker-project

## 2. Build and start all services

docker-compose up --build -d

## 3. Access the apps

App 1 → http://localhost/app1

App 2 → http://localhost/app2

Each route is handled by the NGINX reverse proxy and forwarded to the correct Flask app running in its own container.


## Output

http://localhost/app1 → Hello from App 1!
http://localhost/app2 → Hello from App 2!
