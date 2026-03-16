# AI Resume Builder

A comprehensive AI-powered resume building platform with Spring Boot backend and React frontend.

## Features

### Backend (Spring Boot)
- **JWT Authentication**: Secure user authentication with cookie and header-based token support
- **User Management**: Registration, login, profile management
- **Resume Management**: Create, edit, and manage resumes
- **ATS Scanning**: Check resume compatibility with Applicant Tracking Systems
- **Template System**: Multiple professional resume templates
- **Analytics Dashboard**: Track user activity and engagement
- **Notification System**: Real-time notifications for users
- **Blog Management**: Content management for career resources
- **Subscription Plans**: Premium features and pricing tiers

### Frontend (React)
- **Modern UI**: Built with React, TailwindCSS, and modern UI components
- **Resume Builder**: Interactive resume creation and editing
- **Template Gallery**: Browse and select from multiple templates
- **ATS Checker**: Analyze resume compatibility
- **Dashboard**: Personal analytics and activity tracking
- **Responsive Design**: Mobile-friendly interface
- **Real-time Notifications**: Live notification updates

## Technology Stack

### Backend
- **Spring Boot 3.5.11** - Main framework
- **Spring Security** - Authentication and authorization
- **Spring Data JPA** - Database operations
- **JWT (JSON Web Tokens)** - Token-based authentication
- **MySQL/H2** - Database
- **Maven** - Build tool

### Frontend
- **React 19.2.0** - UI framework
- **Vite** - Build tool and dev server
- **TailwindCSS** - CSS framework
- **React Router** - Navigation
- **Axios** - HTTP client
- **Lucide React** - Icons

## Quick Start

### Prerequisites
- Java 17+
- Node.js 18+
- Maven 3.6+
- MySQL (optional, can use H2 for development)

### Backend Setup
```bash
cd Java_backend
mvn spring-boot:run
```

The backend will start on `http://localhost:8081`

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

The frontend will start on `http://localhost:5173`

### Default Admin User
- **Email**: admin@example.com
- **Password**: admin123

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/forgot-password` - Password reset

### Dashboard
- `GET /api/dashboard/summary` - Dashboard summary
- `GET /api/dashboard/stats` - User statistics

### Notifications
- `GET /api/notifications/user` - User notifications
- `PUT /api/notifications/{id}/read` - Mark as read

### Analytics
- `POST /api/analytics/page-view` - Track page views
- `GET /api/analytics/user-stats` - User analytics

## Database Configuration

The application supports both MySQL and H2 databases:

### MySQL (Production)
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/login_app
spring.datasource.username=root
spring.datasource.password=your_password
```

### H2 (Development)
```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=
```

## Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Encryption**: BCrypt password hashing
- **CORS Configuration**: Cross-origin resource sharing
- **Role-based Access**: USER and ADMIN roles
- **Cookie Security**: HttpOnly cookies for tokens

## Project Structure

```
├── Java_backend/                 # Spring Boot backend
│   ├── src/main/java/           # Java source code
│   │   ├── controller/          # REST controllers
│   │   ├── service/             # Business logic
│   │   ├── repository/          # Data access layer
│   │   ├── entity/              # JPA entities
│   │   ├── dto/                 # Data transfer objects
│   │   ├── security/            # Security configuration
│   │   └── config/              # Application configuration
│   └── src/main/resources/      # Configuration files
├── frontend/                    # React frontend
│   ├── src/
│   │   ├── components/          # React components
│   │   ├── pages/               # Page components
│   │   ├── services/            # API services
│   │   └── utils/               # Utility functions
│   └── public/                  # Static assets
└── README.md                    # This file
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions, please open an issue in the GitHub repository.

---

**Note**: This is a full-stack application that demonstrates modern web development practices with Spring Boot and React.
