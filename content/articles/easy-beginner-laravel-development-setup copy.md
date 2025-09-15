---
title: "Beginner Development Setup + Laravel"
description: "A comprehensive setup guideline for Laravel development using Laravel Herd and Laravel Daily starter kit"
published: 2025/01/15
slug: "easy-beginner-laravel-development-setup"
---

This comprehensive setup guideline is designed for beginners who want to start building Laravel applications quickly and efficiently. Whether you're new to web development or transitioning from other frameworks, this guide will get you up and running with a development-ready Laravel development environment in minutes.

We'll use Laravel Herd for effortless local development and the Laravel Daily starter kit to provide a solid foundation with authentication, user management, and common features already configured - so you can start coding your first Laravel application right away.

## Prerequisites

Before starting, ensure you have these installed:

### Required Software
- **macOS or Windows** (Laravel Herd supports both platforms)
- **VS Code** - [Download VS Code](https://code.visualstudio.com/)

---

# Step 1: Install Laravel Herd

![Laravel Herd](/articles/herd.png)

Laravel Herd is the official Laravel development environment for macOS and Windows. It provides PHP, Nginx, and database services out of the box.

### Download and Install Herd

**For macOS:**
1. Visit [Laravel Herd](https://herd.laravel.com/)
2. Download the latest version for macOS
3. Install the application
4. Launch Herd from your Applications folder

**For Windows:**
1. Visit [Laravel Herd for Windows](https://herd.laravel.com/windows)
2. Download the latest version for Windows
3. Install the application
4. Launch Herd from your Start menu

### Verify Installation
Open Terminal (macOS) or PowerShell (Windows) and run:
```bash
herd --version
php --version
```

Herd automatically manages PHP versions and provides a local development server.

---

# Step 2: Create Project

We'll use the Laravel Daily starter kit which includes authentication, user management, and common features.

### Create Project with Starter Kit
```bash
laravel new my-laravel-app --using=laraveldaily/starter-kit
cd my-laravel-app
```

**Reference**: [Laravel Daily Starter Kit](https://github.com/LaravelDaily/Laravel-Starter-Kit)

---

# Step 3: Env Configuration

### Copy Environment File
```bash
cp .env.example .env
```

### Generate Application Key
```bash
php artisan key:generate
```

---

# Step 4: Database Setup

Laravel 12 comes with SQLite as the default database, which is perfect for development and testing. However, you can also use MySQL, PostgreSQL, or other databases.

### Default SQLite Configuration (Laravel 12)

Laravel 12 uses SQLite by default, which requires no additional setup. The database file will be created automatically in your project's `database/` directory.

Your `.env` file should already be configured for SQLite:
```env
DB_CONNECTION=sqlite
DB_DATABASE=database/database.sqlite
```

### Create SQLite Database File
If the SQLite database file doesn't exist, create it:
```bash
touch database/database.sqlite
```

### Run Migrations
```bash
php artisan migrate
```

### Seed Database (if using starter kit)
```bash
php artisan db:seed
```

---

# Database Management Tools

![Beekeeper Studio](https://www.beekeeperstudio.io/assets/img/screenshots/view-dark-844f0c0d0cb7eb908bae2dfc290786243e4b44530ce9239fcea854d71ec0934625ba5333b276d2014ad116d164dacffb87d5d1fb5b099cf68cc4e799f161fce8.png)

**Beekeeper Studio** - [Download](https://www.beekeeperstudio.io/) (Free, cross-platform database client)

Beekeeper Studio is a modern, open-source SQL editor and database manager that supports:
- **SQLite** (perfect for Laravel 12's default database)
- **MySQL** 
- **PostgreSQL**
- **SQL Server**
- **MariaDB**
- **CockroachDB**

It provides a clean, intuitive interface for managing your databases, writing queries, and viewing data.

---

# Step 5: Compile Asset

### Install Dependencies
```bash
npm install
```

### Development Build
```bash
npm run dev
```

### Production Build
```bash
npm run build
```

---

# Step 6: Start Development Server

### Using Herd
Herd automatically serves your Laravel applications. Your app will be available at:
```
http://my-laravel-app.test
```

### Using Artisan Serve
```bash
php artisan serve
```
Your application will be available at `http://localhost:8000`.

---

# VS Code Extensions

Install these essential extensions for Laravel development:

- **Laravel Extension Pack** - [Install](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel-extension-pack)
- **PHP Intelephense** - [Install](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client)
- **Laravel Blade Snippets** - [Install](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel-blade)
- **Laravel Artisan** - [Install](https://marketplace.visualstudio.com/items?itemName=ryannaddy.laravel-artisan)

---

# Project Structure Overview

Understanding Laravel's directory structure:

```
app/
├── Http/
│   ├── Controllers/     # Application logic
│   ├── Middleware/      # HTTP middleware
│   ├── Requests/       # Form validation
│   └── Resources/      # API resources
├── Models/              # Eloquent models
├── Providers/          # Service providers
└── Services/           # Business logic services

config/                 # Configuration files
database/
├── migrations/         # Database schema
├── seeders/           # Database seeders
└── factories/         # Model factories

resources/
├── views/             # Blade templates
├── css/               # Stylesheets
├── js/                # JavaScript files
└── lang/              # Language files

routes/
├── web.php            # Web routes
├── api.php            # API routes
├── console.php        # Console commands
└── channels.php       # Broadcast channels
```

### Herd Issues
- Restart Herd from the menu bar
- Check Herd's status in the application
- Verify PHP version compatibility

## References and Resources

- [Laravel Documentation](https://laravel.com/docs)
- [Laravel Herd for macOS](https://herd.laravel.com/)
- [Laravel Herd for Windows](https://herd.laravel.com/windows)
- [Laravel Daily Starter Kit](https://github.com/LaravelDaily/Laravel-Starter-Kit)

## Conclusion

This setup provides a modern, efficient Laravel development environment. Laravel Herd simplifies local development, while the Laravel Daily starter kit gives you a solid foundation for building applications. Remember to keep your dependencies updated and follow Laravel's best practices.

Happy coding! 🚀
