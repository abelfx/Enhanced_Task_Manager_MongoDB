# 📝 Task Management REST API (Go + Gin)
**This project is a simple Task Management REST API built using Go, the Gin Web Framework, and MongoDB as the database. It includes JWT-based authentication and authorization and supports full CRUD operations with role-based access control.**

**🚀 Features**
- ✅ User registration and login with hashed passwords
- ✅ JWT-based authentication and protected routes
- ✅ Role-based access control (admin & user)
- ✅ Admins can promote users to admin
- ✅ Create, retrieve, update, and delete tasks (CRUD)
- ✅ Modular and clean folder structure
- ✅ MongoDB integration

📂 Folder Structure
```task_manager/
task_manager/
├── main.go                   # App entry point
├── controllers/              # HTTP handlers
│   └── task_controller.go
│   └── user_controller.go
├── models/                   # Data models
│   ├── task.go
│   └── user.go
├── data/                     # Business logic & data layer
│   ├── task_service.go
│   └── user_service.go
├── middleware/               # JWT & Role auth middleware
│   └── auth_middleware.go
├── router/                   # Route configuration
│   └── router.go
├── docs/                     # Documentation
│   └── api_documentation.md
└── go.mod                    # Go module definition

```


🛠️ Getting Started
1. Clone the repository
```
git clone https://github.com/your-username/task_manager.git
cd task_manager
```
2. Install Dependencies
```
go mod tidy
go get go.mongodb.org/mongo-driver/mongo
go get github.com/golang-jwt/jwt/v5
go get golang.org/x/crypto/bcrypt
go get github.com/gin-gonic/gin
```
3. Run the Application
```go run main.go```

4. Default Base URL
```http://localhost:8080```

**🔐 Authentication & Roles**
- Register new users using /register
- Login with /login to receive a JWT
- Include the token in the Authorization header for protected routes:
  ```
  Authorization: Bearer <your_token>
  ```
- First registered user becomes admin
- Admins can promote others using /promote Endpoint

**🧪 API Endpoints**
- Full API reference including request/response examples is available in the documentation below.

- 📄 docs/api_documentation.md


🔍 API Documentation For full details on how to use the API (request/response formats), go to:

📄 docs/api_documentation.md
