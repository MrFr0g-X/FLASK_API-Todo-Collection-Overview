# 🐍📋 FLASK\_API ✅ Todo Collection

## 🌐 Overview

This is a simple RESTful API for managing 📋 to-do items, built with 🐍 Flask. The API supports creating ✏️, reading 📖, updating 🔄, and deleting 🗑️ (CRUD) to-do items, providing an easy way to maintain a list 📝 of tasks.

This repository includes:

- **🐍 Flask API** with 🔒 authentication middleware and modular route definitions.
- **📝 Swagger Documentation** for interactive API documentation.
- **📮 Postman Collection** for testing 🧪 and interacting with the API.

### ✨ Features

- CRUD operations for managing 📋 to-do items.
- Simple in-memory storage (no external 🗄️ database required).
- 🔒 Authentication middleware to secure the API.

## 📂 Project Structure

```
FLASK_API/
├── app.py               # Older entry point (kept for reference)
├── main.py              # Main entry point that initializes the app and registers blueprints
├── requirements.txt     # 📦 Dependencies for the project
├── swagger.yaml         # 📝 Swagger documentation for the API
├── middleware/          # Middleware folder
│   └── auth.py          # 🔒 Authentication middleware
├── routes/              # Folder for route files
│   └── todo.py          # 🛤️ Blueprint with CRUD operations for todos
└── PostmanCollection/   # Folder containing Postman collection
    └── FLASK_API_Todo_Collection.json # 📮 Postman collection file for API testing
```

## 🚀 Getting Started

### ✅ Prerequisites

- 🐍 Python 3.x
- [📮 Postman](https://www.postman.com/downloads/) for API testing (optional)

### ⚙️ Installation

1. **📥 Clone the Repository**

   ```bash
   git clone https://github.com/MrFr0g-X/FLASK_API-Todo-Collection-Overview.git
   cd FLASK_API-Todo-Collection-Overview

   ```

2. **📦 Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **▶️ Run the Application**

   ```bash
   python main.py
   ```

   The server will start on `http://localhost:3000`.

## 📜 Requirements

The required 🐍 Python packages are listed in `requirements.txt`. These packages include:

```
Flask==2.1.2
```

Add any additional packages you need for your middleware or other components.

## 📄 API Documentation

- **📝 Swagger**: You can view the interactive API documentation using [Swagger Editor](https://editor.swagger.io/). Simply paste the contents of `swagger.yaml` into the editor to explore the available endpoints.

## 🔗 API Endpoints

### 🌍 Base URL

- `http://localhost:3000/todos/`

### 🛤️ Endpoints

1. **GET** `/todos/` - Get all to-do items 📋

   - **Response**: Returns a list of all to-do items.

2. **POST** `/todos/` - Add a new to-do item ➕

   - **Headers**: `Authorization: Bearer mysecrettoken`
   - **Body** (📄 JSON):
     ```json
     {
       "title": "First Todo"
     }
     ```
   - **Response**: Returns the newly created to-do item.

3. **GET** `/todos/{id}` - Get a to-do item by ID 🆔

   - **Headers**: `Authorization: Bearer mysecrettoken`
   - **Response**: Returns the specified to-do item.

4. **PUT** `/todos/{id}` - Update an existing to-do item by ID 🔄

   - **Headers**: `Authorization: Bearer mysecrettoken`
   - **Body** (📄 JSON):
     ```json
     {
       "title": "Updated Todo",
       "completed": true
     }
     ```
   - **Response**: Returns the updated to-do item.

5. **DELETE** `/todos/{id}` - Delete a to-do item by ID 🗑️

   - **Headers**: `Authorization: Bearer mysecrettoken`
   - **Response**: Returns a `204 No Content` status.

## 📮 Postman Collection

A 📮 Postman collection named **"FLASK\_API Todo Collection"** has been created to test all the API endpoints. Follow these steps:

1. **📥 Import the Collection**:
   - In Postman, click **Import** and select the Postman collection file (`PostmanCollection/FLASK_API_Todo_Collection.json`).
2. **▶️ Run the Requests**:
   - The collection includes all CRUD operations (`GET`, `POST`, `PUT`, `DELETE`) for the API.

## 🧪 Testing with Postman

1. **Add 🔒 Authorization Header** to requests that require authentication.
   - **Key**: `Authorization`
   - **Value**: `Bearer mysecrettoken`
2. **Use Postman Runner** to run the entire collection to automate testing of all endpoints.

## 🔒 Authentication

The API uses a simple token-based 🔑 authentication system. Ensure that the `Authorization` header is set with the correct token (`Bearer mysecrettoken`) for requests that require authentication.

## 📝 Swagger Documentation

The `swagger.yaml` file provides a full description of the API, including the expected input/output and response codes. To use Swagger documentation:

- **Open Swagger Editor**: Paste the contents of `swagger.yaml` to view an interactive version of your API documentation.

## 📜 License

This project is licensed under the MIT License - see the [📄 LICENSE](LICENSE) file for details.

