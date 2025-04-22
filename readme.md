# Docker Networking: phpMyAdmin + MySQL

This project sets up two Docker containers:

- **Container A**: phpMyAdmin (web UI for managing MySQL)
- **Container B**: MySQL server

Both containers are connected through a custom Docker network, allowing phpMyAdmin to manage the MySQL server seamlessly.

---

## 🛠️ Setup Instructions

### 1. Clone or Download this Repository

If you haven't already:

git clone <github.com/heinthant/docker-networking>

cd "Docker networking"

2. Start the Containers
3. 
Make sure Docker and Docker Compose are installed on your system. Then run:

docker-compose up -d
This will:

Launch a MySQL server (mysql_container)

Launch a phpMyAdmin instance (phpmyadmin_container)

Expose phpMyAdmin on port 8080 (or 8081, depending on your config)

🌐 Access phpMyAdmin
Open your browser and go to:

http://localhost:8080
Or use http://localhost:8081 if you've changed the port.

Login Credentials:

Field	Value
Server	mysql_container
Username	root
Password	rootpassword
You can also use:

Username: testuser

Password: testpassword

📦 Environment Details
MySQL Container:
Image: mysql:8.0

Database: testdb

User: testuser

Password: testpassword

phpMyAdmin Container:
Image: phpmyadmin/phpmyadmin

Port: 8080 -> 80 (host:container)

🧼 Cleanup
To stop and remove the containers:

docker-compose down
To also remove the database volume:

docker-compose down -v
🐳 Notes
Make sure port 8080 is free before starting the containers.

You can change exposed ports in docker-compose.yml if needed.

📁 Project Structure
Docker networking/

├── docker-compose.yml

└── README.md

🚀 Happy Dockering!
