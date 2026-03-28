# Laravel Docker Setup

## 📦 Stack

* PHP (php-fpm)
* Nginx
* MySQL
* Docker & Docker Compose

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Asadbek2607/docker_lara.git
cd docker_lara
```

---

### 2. Start containers

```bash
docker compose up -d --build
```

---

### 3. Install dependencies

```bash
docker run --rm -v ${PWD}:/app -w /app composer install
```

---

### 4. Generate app key

```bash
docker exec -it myphp php artisan key:generate
```

---

### 5. Run migrations

```bash
docker exec -it myphp php artisan migrate
```

---

## 🌐 Access

* App: http://localhost:9000
* MySQL:

    * Host: 127.0.0.1
    * Port: 3306
    * Database: laravel
    * Username: laravel
    * Password: laravel

---

## 🛠 Useful Commands

### Stop containers

```bash
docker compose down
```

---

### Restart containers

```bash
docker compose up -d
```

---

### View logs

```bash
docker compose logs
```

---

### Run Artisan commands

```bash
docker exec -it myphp php artisan <command>
```

Example:

```bash
docker exec -it myphp php artisan migrate
```

---

## 📁 Project Structure

```text
.
├── app/
├── bootstrap/
├── config/
├── database/
├── nginx/
│   └── default.conf
├── public/
├── routes/
├── docker-compose.yml
├── Dockerfile
└── ...
```

---

## ⚠️ Notes

* `.env` file is not included in the repository
* Copy `.env.example` and configure environment variables
* MySQL data is stored in a Docker volume (`db_data`)

---

## 📌 Requirements

* Docker
* Docker Compose

---

## 💡 Next Steps

* Add Vue (Vite + Node container)
* Optimize Dockerfile for production
* Add CI/CD (GitHub Actions)

---
