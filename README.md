# Smart Driver Application

A modern web application for managing driver services with features for both drivers and passengers.

## Features

### Authentication
- User registration and login
- Password recovery system
  - Forgot password functionality
  - Email-based password reset
  - Secure token-based verification
- Session management
- Role-based access control

### Driver Features
- Profile management
- Ride request handling
- Real-time location tracking
- Earnings management
- Ride history

### Passenger Features
- User profile management
- Ride booking
- Payment integration
- Ride history
- Driver rating system

### Admin Features
- User management
- Driver verification
- Payment monitoring
- Analytics dashboard
- Support system

## Technology Stack

### Frontend
- Angular 15+
- Bootstrap 5
- Material Design
- Socket.IO Client
- Chart.js for analytics
- Google Maps API

### Backend
- Node.js
- Express.js
- MongoDB
- Socket.IO
- JWT Authentication
- Nodemailer for emails

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- Angular CLI
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/smart-driver.git
cd smart-driver
```

2. Install backend dependencies
```bash
cd backend
npm install
```

3. Install frontend dependencies
```bash
cd ../frontend
npm install
```

4. Set up environment variables
Create `.env` file in the backend directory:
```env
PORT=4000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password
```

5. Start the development servers

Backend:
```bash
cd backend
npm run dev
```

Frontend:
```bash
cd frontend
ng serve
```

The application will be available at `http://localhost:4200`

## Password Reset Flow

1. User clicks "Forgot Password" on the login page
2. Enters their email address
3. Receives a password reset link via email
4. Clicks the link to access the reset password page
5. Enters and confirms new password
6. Gets redirected to login with success message

## API Endpoints

### Authentication
- POST `/auth/register` - User registration
- POST `/auth/login` - User login
- POST `/auth/forgot-password` - Request password reset
- POST `/auth/reset-password/:token` - Reset password
- POST `/auth/verify-email` - Email verification

### User Management
- GET `/users/profile` - Get user profile
- PUT `/users/profile` - Update user profile
- GET `/users/rides` - Get user ride history

### Driver Operations
- POST `/drivers/rides` - Accept ride request
- PUT `/drivers/location` - Update driver location
- GET `/drivers/earnings` - Get driver earnings

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Security

- JWT-based authentication
- Password hashing with bcrypt
- Rate limiting on API endpoints
- Input validation and sanitization
- CORS configuration
- Secure password reset flow

## Error Handling

The application implements comprehensive error handling:
- Form validation errors
- API error responses
- Network error handling
- User-friendly error messages
- Logging system for debugging

## Testing

```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
ng test
```

## Deployment

1. Build the frontend
```bash
cd frontend
ng build --prod
```

2. Deploy backend
```bash
cd backend
npm run build
npm start
```

## Support

For support, email support@smartdriver.com or join our Slack channel.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
