# The Photo Lounge ATL - Full Stack Photo Booth Rental Website

A modern full-stack web application for managing photo booth rentals.

## Project Structure

```
The-photolounge-Atlanta/
├── frontend/                 # Angular web application
│   ├── src/
│   │   ├── app/             # Angular components & services
│   │   ├── assets/          # Static files
│   │   ├── main.ts          # Entry point
│   │   └── index.html       # HTML template
│   ├── package.json         # Node.js dependencies
│   ├── angular.json         # Angular configuration
│   └── README.md            # Frontend documentation
│
├── backend/                 # Python Flask API
│   ├── app.py               # Flask application factory
│   ├── models.py            # SQLAlchemy database models
│   ├── routes.py            # API endpoints
│   ├── config.py            # Configuration management
│   ├── requirements.txt      # Python dependencies
│   ├── .env.example         # Environment variable template
│   └── README.md            # Backend documentation
│
├── database/                # Database configuration
│   ├── schema.sql           # Database schema (PostgreSQL)
│   └── README.md            # Database setup documentation
│
└── README.md               # This file
```

## Stack Overview

### Frontend
- **Framework**: Angular 17
- **Language**: TypeScript
- **Styling**: SCSS
- **HTTP Client**: Axios
- **Package Manager**: npm

### Backend
- **Framework**: Flask 3.0
- **Language**: Python 3.8+
- **Database ORM**: SQLAlchemy 2.0
- **Database**: PostgreSQL / SQLite

### Database
- **Primary**: PostgreSQL (production)
- **Development**: SQLite
- **Tables**: Bookings, Availability, Pricing, Reviews

## Quick Start

### 1. Frontend Setup
```bash
cd frontend
npm install
npm start
```
Frontend: http://localhost:4200

### 2. Backend Setup
```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```
Backend API: http://localhost:5000

### 3. Database
- SQLite (auto-created on first run)
- PostgreSQL setup: See `database/README.md`

## Features

### 🎉 Photo Booth Management
- Browse services (weddings, birthdays, corporate, social events)
- Real-time availability checking
- Instant booking requests
- Dynamic pricing calculation

### 💼 Admin Features
- Manage bookings and statuses
- Availability calendar management
- Pricing tier management
- Customer reviews and ratings

### 📱 Responsive Design
- Mobile-friendly interface
- Desktop optimization
- Cross-browser compatibility

## API Documentation

### Base URL
```
http://localhost:5000/api
```

### Main Endpoints

**Bookings**
- `GET /bookings` - List all bookings
- `POST /bookings` - Create new booking
- `GET /bookings/:id` - Get booking details
- `PUT /bookings/:id` - Update booking
- `DELETE /bookings/:id` - Cancel booking

**Availability**
- `GET /availability` - Get available dates

**Pricing**
- `GET /pricing` - Get all pricing tiers
- `GET /pricing/:type` - Get specific event type pricing

**Reviews**
- `GET /reviews` - Get all reviews
- `POST /reviews` - Submit new review

## Configuration

### Environment Variables

**Frontend** (`frontend/.env`)
```
ANGULAR_APP_API_URL=http://localhost:4200
```

**Backend** (`backend/.env`)
```
FLASK_ENV=development
DATABASE_URL=sqlite:///photolounge.db
SERVER_PORT=5000
```

## Development

### Testing

**Frontend**
```bash
cd frontend
npm test
```

**Backend**
```bash
cd backend
python -m pytest
```

### Building for Production

**Frontend**
```bash
cd frontend
npm run build
```

**Backend**
```bash
# Set production environment
export FLASK_ENV=production
gunicorn -w 4 -b 0.0.0.0:5000 app:create_app()
```

## Deployment

### Recommended Hosting

**Frontend**
- Vercel
- Netlify
- AWS S3 + CloudFront
- GitHub Pages

**Backend**
- Heroku
- AWS EC2
- DigitalOcean
- Railway.app

**Database**
- AWS RDS
- Digital Ocean Managed Databases
- Heroku Postgres

## Contact & Support

- **Phone**: (404) 499-6355
- **Email**: atlphotolounge@gmail.com
- **Instagram**: @the_photolounge_co

## License

MIT License - See LICENSE file for details
