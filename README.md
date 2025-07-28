# Utility Container Demo – PHP Dockerized Project

This project sets up a fully containerized local development environment using **Docker Compose**. It includes services for:

- **NGINX** (web server)
- **PHP-FPM 7.4** (application runtime)
- **MySQL 5.7** (database)
- Optional support for **Composer** and **Artisan** commands

---

## 📁 Project Structure

php-dockerized/
├── docker-compose.yaml
├── dockerfile/
│ ├── php.dockerfile
│ └── composer.dockerfile
├── nginx/
│ └── nginx.conf
├── src/
│ └── [Your Laravel or PHP project files]
└── env/
└── mysql.env


---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ajitheaswari/Utility-container-demo.git
cd Utility-container-demo/php-dockerized

2. Build and start the containers
docker-compose up -d --build

3. Access the application
Open your browser at: http://localhost:8000

docker-compose exec php php artisan migrate
docker-compose exec php php artisan serve


