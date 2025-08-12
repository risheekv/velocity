# 🚗 RideFast - Ride Sharing Application

A modern ride-sharing application similar to Rapido or Ola, built with Next.js frontend and Spring Boot backend.

## ✨ Features

### 🚀 User Features
- **User Registration & Authentication** - Secure signup and login system
- **Ride Booking** - Easy ride booking with real-time driver matching
- **Payment Integration** - Secure payment processing
- **Ride History** - Track all your past and current rides
- **Profile Management** - Update personal information and preferences

### 🚗 Driver Features
- **Driver Registration** - Complete driver onboarding with license verification
- **Ride Management** - Accept, start, and complete rides
- **Earnings Dashboard** - Track earnings and ride statistics
- **Location Services** - Real-time location tracking

### 🏢 Company Features
- **Admin Dashboard** - Monitor all rides and drivers
- **Analytics** - Business insights and performance metrics

## 🛠️ Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **Material-UI** - React component library
- **Redux Toolkit** - State management
- **Formik & Yup** - Form handling and validation
- **Axios** - HTTP client

### Backend
- **Spring Boot 3** - Java framework
- **Spring Security** - Authentication and authorization
- **Spring Data JPA** - Database operations
- **MySQL** - Database
- **JWT** - Token-based authentication
- **ModelMapper** - Object mapping
- **Maven** - Build tool

### DevOps & Tools
- **Docker** - Containerization
- **Git** - Version control

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- Java 17+
- MySQL 8.0+
- Maven 3.6+

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd ride_fast
   ```

2. **Configure Database**
   - Create MySQL database
   - Update `ride_fast_backend/src/main/resources/application.yml` with your database credentials

3. **Run Backend**
   ```bash
   cd ride_fast_backend
   ./mvnw spring-boot:run
   ```
   Backend will start on `http://localhost:8081`

### Frontend Setup

1. **Install Dependencies**
   ```bash
   cd ride_fast_frontend
   npm install
   ```

2. **Run Development Server**
   ```bash
   npm run dev
   ```
   Frontend will start on `http://localhost:3000`

## 📁 Project Structure

```
ride_fast/
├── ride_fast_backend/          # Spring Boot backend
│   ├── src/main/java/
│   │   └── com/ridefast/ride_fast_backend/
│   │       ├── controller/     # REST controllers
│   │       ├── service/        # Business logic
│   │       ├── repository/     # Data access layer
│   │       ├── model/          # Entity classes
│   │       ├── dto/            # Data transfer objects
│   │       └── config/         # Configuration classes
│   └── src/main/resources/
│       └── application.yml     # Application configuration
├── ride_fast_frontend/         # Next.js frontend
│   ├── app/                    # App Router pages
│   ├── components/             # React components
│   ├── utils/                  # Utilities and Redux store
│   └── public/                 # Static assets
└── README.md
```

## 🔧 Configuration

### Environment Variables

**Backend** (`application.yml`):
```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/ride_fast_db
    username: your_username
    password: your_password
```

**Frontend** (`next.config.mjs`):
```javascript
// API proxy configuration
async rewrites() {
  return [
    {
      source: "/api/:path*",
      destination: "http://localhost:8081/api/:path*",
    },
  ];
}
```

## 🚀 Deployment

### Backend Deployment
```bash
cd ride_fast_backend
./mvnw clean package
java -jar target/ride_fast_backend-0.0.1-SNAPSHOT.jar
```

### Frontend Deployment
```bash
cd ride_fast_frontend
npm run build
npm start
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Risheek** - *Full Stack Developer*

- GitHub: [@risheek](https://github.com/risheek)
- LinkedIn: [Your LinkedIn]

## 🙏 Acknowledgments

- Spring Boot team for the excellent framework
- Next.js team for the amazing React framework
- All contributors and supporters

---

⭐ Star this repository if you found it helpful!
