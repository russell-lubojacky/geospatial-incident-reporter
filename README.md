# 🌍 Geospatial Incident Reporter (Open Source)

A full-stack open-source web application that allows users to report, visualize, and analyze environmental and infrastructure incidents on an interactive map. AI models analyze text and images to classify severity and recommend actions in real-time.

## 🚀 Features

- 📍 Report incidents with location, photo, and description
- 🧠 AI-powered classification using open models (text & image)
- 🗺 Interactive map with clustered markers, filters, and heatmaps
- 🔍 Search and filter by severity, type, or proximity
- 🌐 REST API with OpenAPI/Swagger docs
- 🔄 Offline-first support (PWA)
- 🛠 Admin dashboard with analytics and moderation tools

## 🧱 Tech Stack

### Frontend
- SvelteKit (or Angular/React)
- Leaflet.js / MapLibre GL (OpenStreetMap-based)
- Tailwind CSS

### Backend
- Node.js (Express or Fastify)
- PostgreSQL + PostGIS
- Redis (for caching and background jobs)
- Python FastAPI (for AI microservice)

### AI Services
- Hugging Face Transformers (text classification)
- CLIP (Contrastive Language-Image Pretraining)
- OpenCV or PIL for image preprocessing

### DevOps
- Docker + Docker Compose
- GitHub Actions for CI/CD
- Flyway or Sqitch for database migrations

## 📸 Example Use Case

> A user sees a flooded trail in a national park. They take a photo, describe the issue, and submit the report. The system:
> - Geolocates the photo or user input
> - Uses an AI model to tag the incident as "flooding"
> - Automatically adds the report to a public map
> - Notifies the park's maintenance system (via webhook or API)

## 📂 Project Structure 
```
geospatial-incident-reporter/ 
├── client/ # SvelteKit frontend 
├── server/ # Node.js API 
├── ai-service/ # Python FastAPI for AI models 
├── database/ # PostgreSQL schema and migrations
├── workflows/  
├── docs/ # Architecture diagrams, API specs 
├── .github/ # GitHub Actions workflows 
└── docker-compose.yml 
```

## 🧪 Local Development

```bash
# Clone the repo
git clone https://github.com/your-username/geospatial-incident-reporter.git
cd geospatial-incident-reporter

# Start all services
docker-compose up --build
```

Visit http://localhost:5173 for the app, http://localhost:3000/api/docs for Swagger UI.

## 📈 Roadmap
- User authentication with OAuth2
- Role-based permissions (reporter, moderator, admin)
- Integration with local government APIs
- Mobile app version (via Capacitor)

## 🤝 Contributing
Pull requests are welcome! Please open an issue first to discuss any major changes.

## 📄 License
MIT

> Disclaimer: This is an independent project for educational and demonstration purposes. It is not affiliated with or endorsed by any government agency.