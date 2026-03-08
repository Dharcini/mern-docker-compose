## Commands Used During the Project
**Clone the repository**
git clone https://github.com/<your-username>/mern-docker-compose.git
**Build Docker images**
docker build -t mern-frontend .
docker build -t mern-backend .
**Create a Docker network**
docker network create mern
**Run Containers**
docker run --network=mern --name backend -d -p 5050:5050 mern-backend
docker run --network=mern --name frontend -d -p 5173:5173 mern-frontend
docker run --network=mern --name mongodb -d -p 27017:27017 -v mongo-data:/data/db mongo:latest
**Stop and remove containers**
docker stop frontend backend mongodb
docker rm frontend backend mongodb
**Run the application using Docker Compose**
docker compose up -d --build
**Stop the compose services**
docker compose stop / docker compose down
**Git commands used**
git init
git add .
git commit -m "Containerize MERN"
git branch -M main
git remote add origin https://github.com/Dharcini/mern-docker-compose.git
git push -u origin main
