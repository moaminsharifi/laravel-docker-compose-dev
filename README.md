 **# Laravel Development with Docker Compose**

## Streamline your local Laravel development with Docker Compose! 

This project provides a hassle-free setup for running Laravel locally using Docker Compose. It includes:

- **Laravel 8.x (or compatible)**
- **PHP 8.3**
- **MariaDB**
- **Redis**
- **Optimized permissions for seamless file handling**

**Key Features:**

- **Simple setup:** Get your Laravel environment up and running quickly.
- **Development-friendly:** Hot reloading for efficient coding and testing.
- **Permission handling:** Avoid file permission issues between host and containers.
- **Easy maintenance:** Update dependencies and configuration with ease.

**Getting Started:**

1. **Clone this repository:**
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   ```

2. **Set up environment variables:**
   - Copy the `.env.example` file to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Fill in the `USER` and `UID` values in the `.env` file. You can find your UID by typing `id` in your terminal.

3. **Build the Docker images:**
   ```bash
   docker compose -f docker-compose.dev.yml build
   ```

4. **Start the containers:**
   ```bash
   docker compose -f docker-compose.dev.yml up
   ```

5. **Access your application:**
   Visit `http://localhost:8000` in your browser.

**Additional Notes:**

- **Database configuration:** Use `mariadb` as the database host in your Laravel configuration.
- **Redis configuration:** Use `redis` as the Redis host in your Laravel configuration.
- **File permissions:** The `docker-compose.dev.yml` file is configured to map the user and group ID of your host machine to the application container, ensuring smooth file operations.

**Happy developing!**

