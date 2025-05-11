
# 📇 Contact Management System – REST API (Laravel)

A simple and secure **RESTful API** built with **Laravel** for managing contacts. This system allows users to perform CRUD (Create, Read, Update, Delete) operations on contact entries via API endpoints.

---

## ✅ Features

* User Authentication with **Laravel Sanctum**
* Create, view, update, and delete contacts
* RESTful API design
* Input validation & error handling
* JSON responses for all endpoints

---

## 🔧 Technologies Used

| Tech            | Purpose                   |
| --------------- | ------------------------- |
| Laravel         | PHP framework for backend |
| MySQL           | Relational database       |
| Laravel Sanctum | API Authentication        |
| Postman / cURL  | API testing               |
| Composer        | Dependency manager        |
| PHP (8.x)       | Language runtime          |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/contact-management-api.git
cd contact-management-api
```

### 2. Install Dependencies

```bash
composer install
```

### 3. Configure Environment

```bash
cp .env.example .env
php artisan key:generate
```

> Update the `.env` file with your **database** and **mail** credentials.

### 4. Run Migrations

```bash
php artisan migrate
```

### 5. Serve the Application

```bash
php artisan serve
```

The API will be available at:
`http://localhost:8000/api`

---

---

## 🧪 API Endpoints

### 🔑 Auth Routes

| Method | Endpoint        | Description       |
| ------ | --------------- | ----------------- |
| POST   | `/api/register` | Register user     |
| POST   | `/api/login`    | Login & get token |
| POST   | `/api/logout`   | Logout            |

### 📇 Contact Routes (Authenticated)

| Method | Endpoint             | Description        |
| ------ | -------------------- | ------------------ |
| GET    | `/api/contacts`      | List all contacts  |
| POST   | `/api/contacts`      | Create new contact |
| GET    | `/api/contacts/{id}` | Get single contact |
| PUT    | `/api/contacts/{id}` | Update contact     |
| DELETE | `/api/contacts/{id}` | Delete contact     |

> All contact routes require a Bearer token in the `Authorization` header.

---

## 🧾 Sample Contact Payload

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "1234567890",
  "address": "123 Main Street"
}
```

---

## 📂 Project Structure

```
/app
  /Http
    /Controllers/API   # Auth & Contact controllers       
/database/migrations   # User & contact table schemas
```


---
