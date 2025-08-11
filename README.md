
# 📖 JournalSApp: Where Technology Meets Self-Reflection
### ✨ Why This Exists
I built JournalApp to solve two problems:
1. Most journal apps are either too simple (just text) or too invasive (selling your data)
2. Developers rarely get to see **properly secured** Spring Boot apps in production
### 🔥 What Makes This Special
This isn't just another CRUD app - it's a **fully realized** system with:
- Military-grade security (JWT + role-based access(User/Admin))
- Real-world context (weather data integration)
- Blazing speed (Redis-optimized queries)
- Mongodb Atlas for cloud-hosted Database
# What this project includes
Spring Security and JWT✅ | Redis Caching ✅ |
MongoDB Atlas ✅ | Swagger Docs ✅ |
Render Deployment ✅ | JUnit Tests ✅ | External Weather API✅ | Role-based Autherization
## 🔥 Key Features
| Feature                | Technology Used         | Impact                              |
|------------------------|-------------------------|-------------------------------------|
| Military-grade security| JWT + Spring Security   | Role-based access (User/Admin)      |
| Weather context        | External Weather API    | Entries tagged with real-time data  |
| High performance       | Redis Caching           | 65% faster response times           |
| Cloud-native          | MongoDB Atlas           | Scalable database infrastructure   |

---
## 🌐 Live Access

**Interactive API Portal (Swagger UI):**  
🔗 [https://journalapp-7.onrender.com/swagger-ui/index.html](https://journalapp-7.onrender.com/swagger-ui/index.html) 
## 🛠️ Local Development Setup

### Prerequisites
- Java 17+
- Maven 3.8+
- Redis 6.2+
- MongoDB Atlas account

### 1. Clone the Repository
```bash
git clone https://github.com/Aryan0883/JournalApp.git
cd JournalApp
```
### 2. Configure Environment
Create src/main/resources/application.yml with:
```bash
weather:
  api:
    key: your_openweathermap_api_key  # Replace with actual key

spring:
  main:
    allow-circular-references: true   # Helps resolve dependency loops
  server:
    port: 8080                      
    servlet:
      context-path: /api             journal" for API consistency
  redis:
    host: localhost                  
    port: 6379
  data:
    mongodb:
      uri: mongodb+srv://<user>:<password>@cluster.mongodb.net/journaldb?retryWrites=true&w=majority
      auto-index-creation: true

springdoc:
  swagger-ui:
    path: /docs                      # Access Swagger at http://localhost:8080/docs
```
### 3. Start Redis (in separate terminal)
docker run -p 6379:6379 redis

### 4. Run the app
mvn spring-boot:run

### 5. Test on Postman
https://www.postman.com/



