# Fleet Management System for County Governments in Kenya

## Overview
The **Fleet Management System** is designed to help county governments in Kenya efficiently manage, track, and maintain their vehicle fleet. The system ensures proper utilization, reduces costs, tracks vehicle movements, schedules maintenance, and improves accountability.

## Features
### 1. Vehicle Management
- Register county-owned vehicles (plate number, model, department, driver assignment).
- Track insurance, logbooks, and compliance with NTSA regulations.

### 2. GPS Tracking & Live Monitoring
- Real-time GPS tracking via **Google Maps API** or **Mapbox**.
- Geo-fencing to restrict vehicle movement.
- Alerts for unauthorized movement or parking violations.

### 3. Fuel & Expense Tracking
- Monitor fuel purchases and prevent fraud.
- Generate fuel efficiency reports per vehicle.
- Track maintenance and servicing costs.

### 4. Maintenance & Repairs Management
- Schedule and track vehicle servicing.
- Maintenance alerts and history logs.
- Breakdown reporting and repair tracking.

### 5. Driver & Personnel Management
- Store driver details, licenses, and assignments.
- Track driver behavior (speeding, braking, idle time).
- Driver rating and feedback system.

### 6. Trip Scheduling & Route Optimization
- Trip request and approval system.
- Automated route planning for efficiency.
- Vehicle allocation per department.

### 7. Incident & Accident Reporting
- Drivers can report accidents via the app.
- Attach photos, location, and descriptions.
- Insurance claim tracking.

### 8. Reports & Compliance
- Generate reports on vehicle usage, expenses, and incidents.
- Ensure compliance with NTSA and government regulations.
- Audit logs for accountability.

## Technology Stack
```json
{
  "frontend": "Flutter (Dart)",
  "backend": "Node.js (Express.js / NestJS)",
  "database": "PostgreSQL / MySQL / Firebase Firestore",
  "authentication": "Firebase Auth / JWT",
  "maps & gps": "Google Maps API / OpenStreetMap",
  "notifications": "Firebase Cloud Messaging (FCM)",
  "file storage": "Firebase Storage / AWS S3",
  "deployment": "Vercel (Backend) + Firebase Hosting / AWS (Frontend)"
}
```

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- **Flutter** (latest version)
- **Node.js** (LTS version)
- **PostgreSQL / MySQL**
- **Firebase Account** (for authentication & storage)
- **Google Maps API Key**

### 1. Backend Setup (Node.js)
```sh
# Clone the repository
git clone https://github.com/your-repo/fleet-management-system.git
cd fleet-management-system/backend

# Install dependencies
npm install

# Set up environment variables (.env)
PORT=5000
DATABASE_URL=your_database_url
JWT_SECRET=your_jwt_secret
FIREBASE_ADMIN_SDK=your_firebase_credentials
MAPS_API_KEY=your_google_maps_api_key

# Run the server
npm start
```

### 2. Frontend Setup (Flutter)
```sh
# Navigate to the frontend folder
cd fleet-management-system/frontend

# Install dependencies
flutter pub get

# Run the Flutter app
flutter run
```

## API Endpoints
```json
{
  "authentication": {
    "register": "POST /api/auth/register",
    "login": "POST /api/auth/login"
  },
  "vehicle_management": {
    "get_vehicles": "GET /api/vehicles",
    "add_vehicle": "POST /api/vehicles",
    "update_vehicle": "PUT /api/vehicles/:id",
    "delete_vehicle": "DELETE /api/vehicles/:id"
  },
  "gps_tracking": {
    "get_location": "GET /api/tracking/:vehicleId",
    "update_location": "POST /api/tracking/update"
  },
  "trip_management": {
    "request_trip": "POST /api/trips/request",
    "trip_history": "GET /api/trips/history",
    "approve_trip": "PUT /api/trips/:id/approve"
  },
  "incident_reporting": {
    "report_incident": "POST /api/incidents/report",
    "get_incidents": "GET /api/incidents"
  }
}
```

## Deployment
### Backend (Node.js) - Deploying to Vercel
```sh
npm install -g vercel
vercel login
vercel deploy
```

### Frontend (Flutter) - Deploying to Firebase Hosting
```sh
flutter build web
firebase deploy
```

## Contributing
```json
{
  "steps": [
    "Fork the repository",
    "Create a feature branch (git checkout -b feature-name)",
    "Commit changes (git commit -m \"Added new feature\")",
    "Push to branch (git push origin feature-name)",
    "Open a Pull Request"
  ]
}
```

## License
```text
This project is licensed under the MIT License.
```

## Contact
```json
{
  "email": "richardsonreuben78@gmail.com",
  "github": "https://github.com/RichardNzembei",
  "linkedin": "https://linkedin.com/in/your-profile"
}
