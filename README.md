# 🚀 Social Platform

A **full-stack social platform** built with **Laravel (PHP)** for the backend and **Angular 17 + Tailwind CSS** for the frontend.  
The project was developed to demonstrate full-stack development skills.

---

## ✨ Features

- **Authentication**
  - Register new users
  - Login / Logout with token-based authentication

- **Posts**
  - Create new posts with categories
  - Edit and delete your own posts
  - View the global feed of all posts
  - Open single post details

- **Comments**
  - Add comments to posts
  - Delete your own comments
  - Display comment count

- **User Profile**
  - View your own profile with created posts
  - Navigate to profile from the header when logged in

- **UI/UX**
  - Responsive design with Tailwind CSS
  - Navigation bar with conditional links (Login/Register vs. Profile/Logout)
  - Inline form validation for login, register, and post forms

---

## 🛠️ Tech Stack

- **Frontend:** [Angular 17](https://angular.io/), [TypeScript](https://www.typescriptlang.org/), [Tailwind CSS](https://tailwindcss.com/)  
- **Backend:** [Laravel 10](https://laravel.com/) (PHP 8.x), REST API  
- **Database:** [MySQL](https://www.mysql.com/) (via **XAMPP** or standalone server)  
- **Tools:** [Node.js](https://nodejs.org/), [Composer](https://getcomposer.org/), [Visual Studio Code](https://code.visualstudio.com/)  

---

## ⚙️ Installation & Setup

### 1. Prerequisites
Make sure you have installed:
- **PHP 8.x** (included in [XAMPP](https://www.apachefriends.org/))
- **Composer**
- **Node.js** (v18+ recommended)
- **npm** (comes with Node.js)
- **Angular CLI**: npm install -g @angular/cli

## 2️ Backend Setup (Laravel API)

### 2.1 Navigate to the backend folder
cd social-platform-backend

### 2.2 Install dependencies
composer install
### 2.3 Create environment file
Copy the example configuration:
- cp .env.example .env

### 2.4 Configure database (MySQL via XAMPP)
Open .env and update the following lines:

DB_CONNECTION=mysql <br>
DB_HOST=127.0.0.1 <br>
DB_PORT=3306 <br>
DB_DATABASE=social_platform <br>
DB_USERNAME=root <br>
DB_PASSWORD= <br>

Make sure MySQL is running in XAMPP and the database social_platform is created manually via phpMyAdmin or CLI.
### 2.5 Run migrations and seeders
php artisan migrate --seed <br>
This will create tables and insert default categories (Technology, Health, Lifestyle, Travel, Food).

### 2.6 Start backend server
php artisan serve <br>

By default, API will be available at: <br>
(http://127.0.0.1:8000)

## 3. Frontend Setup (Angular App)
### 3.1 Navigate to the frontend folder
cd social-platform-frontend

### 3.2 Install dependencies
npm install

### 3.3 Install dependencies
Open src/environments/environment.ts and update: <br>
export const environment = {
  production: false,
  apiUrl: 'http://127.0.0.1:8000/api/v1'
};


### 3.4 Run Angular app
ng serve --open
By default, frontend will run at: <br>
http://localhost:4200


## 4. Default Data (Seeders)
The project includes a CategorySeeder which seeds 5 default categories: <br>
- Technology
- Health
- Lifestyle
- Travel
- Food <br>

Run this manually anytime with: <br>
php artisan db:seed --class=CategorySeeder

## 5. Login Credentials
After running migrations & seeders, you can register new users via the frontend (/register) or insert manually into the users table.


### Testing Checklist:
- **Auth**: Register → Login → Logout
- **Posts**: Create, edit, delete, list
- **Comments**: Add & delete comments
- **Profile**: View your own posts
- **UI**: Responsive navigation + forms validation












