# 🚖 Ride-Sharing Service Backend

## 📌 Overview
This project is a simplified ride-sharing backend that demonstrates:
- **Code Versioning** → Implement code versioning, Create a git repository and share link when done with the project.
- **Algorithm Design** → Assigning drivers to riders based on distance and availability.
- **API Integration** → Fetching real-time driver locations from an external geolocation API.
- **Code Deployment** → Dockerizing and deploying the service to a cloud platform.

---

## 🚀 Features
✅ **Ride-Matching Algorithm** - Assigns the nearest driver to a rider using the Haversine formula.
✅ **Real-Time Geolocation Fetching** - Integrates with Google Maps API (or OpenStreetMap) to update driver locations.
✅ **Dockerized & Deployed** - Supports docker deployment.
✅ **REST API Endpoints** - Exposes APIs for requesting rides, listing drivers, and tracking rides.

---

## 📂 Project Structure
```
📦 ride-sharing-backend
├── 📂 src
│   ├── 📄 main.go (or app.js / server.py) → API and logic
│   ├── 📄 matching.go (or matching.ts / matching.py) → Ride-matching algorithm
│   ├── 📄 api.go (or api.ts / api.py) → External API integration
│   ├── 📄 config.env → Environment variables
├── 📂 tests → Unit and integration tests
├── 📄 Dockerfile → Containerization setup
├── 📄 docker-compose.yml → Local development setup
├── 📄 .github/workflows/ci-cd.yml → CI/CD pipeline
├── 📄 README.md → Documentation
```

---

## 🛠️ Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/ride-sharing-backend.git
cd ride-sharing-backend
```
### 2️⃣ Set Up Environment Variables
Create a `.env` file and add API keys & configs:
```
PORT=8080
API_KEY=your_api_key_here
REDIS_URL=your_redis_url
```
### 3️⃣ Run with Docker
```bash
docker-compose up --build
```
### 4️⃣ Run Locally
```bash
# If using Go
go run main.go

# If using Node.js
npm install && npm start

# If using Python
pip install -r requirements.txt
python app.py
```

---

## 🔌 API Endpoints
| Method | Endpoint            | Description                        |
|--------|---------------------|------------------------------------|
| POST   | `/request-ride`     | Request a ride, match driver      |
| GET    | `/drivers`          | List available drivers            |
| GET    | `/ride-status/:id`  | Track an ongoing ride             |

Example Request:
```bash
curl -X POST "http://localhost:8080/request-ride" -H "Content-Type: application/json" -d '{ "lat": 40.7128, "lon": -74.0060 }'
```

---

## 🌍 Deployment
### Deploy with Docker
1. **Build & Push to Container Registry** 
```bash
docker build -t ride-sharing-backend .
docker tag ride-sharing-backend your-container-registry/ride-sharing
```
---

## 🧪 Running Tests
```bash
# Run unit tests
go test ./...
# or
npm test
# or
pytest
```

---

## 💡 Future Improvements
🔹 Implement **real-time updates** with WebSockets.  
🔹 Add **payment integration** for ride fare calculation.  
🔹 Enhance **security** with OAuth2 authentication.

---

## 🏆 Contributing
Pull requests are welcome! Please open an issue first for major changes.

---

## 📜 License
MIT License © 2025 True African

