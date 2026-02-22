# 🥩 GKSteak Web - Legacy Restaurant Archive Restoration

**GKSteak Web Restoration** is a specialized project aimed at reviving and containerizing the archive of the original GKSteak website. This project breathes new life into a legacy codebase by packaging it into a modern, plug-and-play **Docker** environment, ensuring its preservation and ease of deployment.

![Status](https://img.shields.io/badge/Status-Restored-success?style=for-the-badge)
![WordPress](https://img.shields.io/badge/WordPress-5.8-blue?style=for-the-badge&logo=wordpress)
![PHP](https://img.shields.io/badge/PHP-7.4-777BB4?style=for-the-badge&logo=php)
![MariaDB](https://img.shields.io/badge/MariaDB-10.6-003545?style=for-the-badge&logo=mariadb)
![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=for-the-badge&logo=docker)

---

## 📸 Archive Showcase

Explore the restored interface of the legacy GKSteak website through our gallery.

| | |
|:---:|:---:|
| ![Home](screenshots/home.png)<br>**Homepage (Frontend)** | ![Menu](screenshots/menu.png)<br>**Restaurant Menu** |
| ![About](screenshots/about.png)<br>**About Us** | ![Login](screenshots/login.png)<br>**Admin Dashboard Login** |

---

## 🚀 Restoration Highlights

### 🛠️ Technical Fixes
*   **Database URL Mapping**: Automatically transforms all legacy links from `gksteak.com` to `localhost:8082` for seamless local browsing.
*   **Custom Table Prefix**: Engineered to support the original backup's unique `wp2o_` database prefix.
*   **Hardcoded Configs**: Optimized `wp-config.php` for the specific restoration environment.

### 🍱 UI/UX Enhancements
*   **Menu Alignment**: Fixed menu titles to be perfectly centered for a cleaner aesthetic.
*   **Currency Normalization**: Removed obsolete currency symbols from the menu items to maintain a modern look.
*   *File Location*: `wp-content/plugins/food-and-drink-menu/fdm-templates/content/`

### 🔄 Persistence & Reliability
*   **Auto-Initialization**: Database is automatically imported from `init.sql` upon first launch.
*   **Self-Healing**: Containers are configured with `restart: always` to ensure uptime across crashes or reboots.

---

## 🛠 Tech Stack

### Core Engine
*   **CMS**: WordPress 5.8 (Classic Restoration)
*   **Environment**: PHP 7.4 (Optimized for Legacy Compatibility)
*   **Database**: MariaDB 10.6

### Infrastructure
*   **Containerization**: Docker & Docker Compose
*   **Automation**: Custom SQL Initialization Scripts

---

## 📂 Project Structure

```bash
/
├── docker-compose.yml   # Infrastructure as Code (Services definition)
├── init.sql             # Legacy Database Dump (Auto-import)
├── wp-config.php        # Core WordPress Configuration
├── wp-content/          # Original Themes, Plugins, and Media Assets
└── screenshots/         # Documentation Assets
```

---

## 📦 Getting Started

### Prerequisites
*   **Docker Engine**
*   **Docker Compose**

### Quick Launch
1.  **Clone** this repository to your local machine.
2.  **Navigate** to the project directory in your terminal.
3.  **Run** the following command:
    ```bash
    docker compose up -d
    ```
4.  **Wait** 1-2 minutes for the database initialization to complete.

### Access Points
*   **Frontend**: [http://localhost:8082](http://localhost:8082)
*   **Admin Dashboard**: [http://localhost:8082/wp-admin](http://localhost:8082/wp-admin)

### 🔑 Credentials
*   **Username**: `gksteak`
*   **Password**: `gksteak123`

---

## ❓ Troubleshooting

*   **Service not responding?** Check status with `docker ps` or logs with `docker compose logs -f`.
*   **Fresh Start?** To reset the environment to the original backup state:
    ```bash
    docker compose down -v
    docker compose up -d
    ```

---

## 👥 Authors

Developed and Restored by **Widi Firmaan**.
