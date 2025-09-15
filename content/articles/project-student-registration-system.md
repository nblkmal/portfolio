---
title: "Project: Student Registration System"
description: "A 1-hour Laravel tutorial for building a simple student registration system with admin and student roles"
published: 2025/01/17
slug: "project-student-registration-system"
---

---

## 📚 **Prerequisites & Setup**

Before starting this tutorial, make sure you have Laravel properly set up on your system. Follow our comprehensive setup guide:

👉 **[Beginner Laravel Development Setup](/articles/easy-beginner-laravel-development-setup)** - Complete Laravel environment setup with Herd and starter kit

This setup guide will walk you through:
- Installing Laravel Herd (macOS/Windows)
- Creating projects with Laravel Daily starter kit
- Database configuration (SQLite by default)
- Essential VS Code extensions
- Development server setup

---

## **Student Registration System**
( 1 Hour Laravel Tutorial )

This tutorial will guide you through building a simple student registration system using Laravel. Perfect for beginners who want to learn Laravel fundamentals while creating a practical application.

## 🎯 Learning Objectives

By the end of this 1-hour session, students will:
- Set up a Laravel project with authentication
- Create user roles (Admin & Student)
- Build student registration functionality
- Implement admin dashboard for user management
- Understand basic Laravel concepts (Models, Controllers, Views, Routes)

## 📋 System Features

### Core Features
1. **Student Registration** - Students can register themselves
2. **Admin Dashboard** - Admin can view all registered students
3. **User Management** - Admin can edit student information
4. **Role-based Access** - Different views for Admin vs Student
5. **Basic Authentication** - Login/logout functionality

## ⏰ 1-Hour Lesson Plan

### Phase 1: Project Setup
- Install Laravel with starter kit
- Configure environment
- Set up database
- Install VS Code extensions

### Phase 2: Database & Models
- Create User model modifications
- Add role field to users table
- Create migration for student data
- Run migrations

### Phase 3: Authentication & Roles
- Set up role-based middleware
- Create Admin and Student controllers
- Implement registration with role assignment
- Test login functionality

### Phase 4: Student Registration
- Create student registration form
- Handle form submission
- Validate student data
- Redirect after successful registration

### Phase 5: Admin Dashboard
- Create admin dashboard view
- Display list of all students
- Add edit functionality
- Test admin features

## 🚀 Implementation Steps

### Step 1: Project Setup
```bash
# Create Laravel project with starter kit
laravel new student-registration --using=laraveldaily/starter-kit
cd student-registration

# Configure environment
cp .env.example .env
php artisan key:generate

# Set up SQLite database
touch database/database.sqlite

# Run migrations
php artisan migrate
php artisan db:seed
```

### Step 2: Database & Models
```bash
# Add role field to users table
php artisan make:migration add_role_to_users_table --table=users

# Create Student model with additional fields
php artisan make:model Student -m
```

**Migration for users table:**
```php
public function up()
{
    Schema::table('users', function (Blueprint $table) {
        $table->enum('role', ['admin', 'student'])->default('student');
        $table->string('student_id')->nullable();
        $table->string('phone')->nullable();
        $table->date('date_of_birth')->nullable();
    });
}
```

### Step 3: Authentication & Roles
```bash
# Create middleware for role checking
php artisan make:middleware CheckRole

# Create controllers
php artisan make:controller AdminController
php artisan make:controller StudentController
```

**Role Middleware:**
```php
public function handle($request, Closure $next, $role)
{
    if (auth()->user()->role !== $role) {
        abort(403, 'Unauthorized');
    }
    return $next($request);
}
```

### Step 4: Student Registration
**Registration Form (resources/views/auth/register.blade.php):**
```html
<form method="POST" action="{{ route('register') }}">
    @csrf
    <input type="text" name="name" placeholder="Full Name" required>
    <input type="email" name="email" placeholder="Email" required>
    <input type="password" name="password" placeholder="Password" required>
    <input type="text" name="student_id" placeholder="Student ID" required>
    <input type="tel" name="phone" placeholder="Phone Number">
    <input type="date" name="date_of_birth" placeholder="Date of Birth">
    <button type="submit">Register as Student</button>
</form>
```

### Step 5: Admin Dashboard
**Admin Controller:**
```php
public function dashboard()
{
    $students = User::where('role', 'student')->get();
    return view('admin.dashboard', compact('students'));
}

public function editStudent($id)
{
    $student = User::findOrFail($id);
    return view('admin.edit-student', compact('student'));
}
```

## 🎯 Testing the Application

1. **Register as Student**: Visit `/register` and create a student account
2. **Login as Admin**: Use seeded admin account (admin@example.com)
3. **View Students**: Admin dashboard shows all registered students
4. **Edit Student**: Admin can modify student information

## 🔮 Future Features (Next Steps)

### 1. Course Management System
- Add courses table and model
- Allow students to enroll in courses
- Admin can create/manage courses
- Student dashboard shows enrolled courses

### 2. Grade Management
- Create grades table linked to students and courses
- Admin can input grades for students
- Students can view their grades
- Grade calculation and GPA system

### 3. Attendance Tracking
- Daily attendance marking system
- Student attendance history
- Attendance reports for admin
- Email notifications for absent students

### 4. Fee Management
- Fee structure for different courses
- Payment tracking system
- Due date notifications
- Payment history for students

### 5. Communication System
- Announcement system for admin
- Student notification center
- Email/SMS integration
- Discussion forums for courses

## 📚 Learning Outcomes

After completing this tutorial, students will understand:
- Laravel MVC architecture
- Database migrations and models
- Authentication and authorization
- Form handling and validation
- Blade templating
- Route management
- Middleware concepts