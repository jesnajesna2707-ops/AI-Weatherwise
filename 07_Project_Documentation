# Phase 7: Project Documentation & API Guide

## 1. Local Deployment Setup Instructions

### 1.1 Prerequisites
* Node.js runtime framework (v16 or above installed).
* MongoDB local engine running or an active MongoDB Atlas cluster cloud link.

### 1.2 Installation Steps
1. Clone this repository locally.
2. Navigate to the backend directory: `cd 05_Project_Development/backend`
3. Install all packages and modules: `npm install`
4. Setup your local environment variables in a `.env` file in the root root folder:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_signature_secret
   GEMINI_API_KEY=your_google_gemini_api_key
   ```
5. Spin up the localized runtime server: `npm run dev`

---

## 2. REST API Documentation Reference

### 2.1 Authentication Gateways
* **POST** `/api/auth/register` - Registers a new system account wrapper. Needs `name`, `email`, and `password` parameters.
* **POST** `/api/auth/login` - Signs users into sessions. Returns a secure JSON Web Token string.

### 2.2 Location Matrix & AI Weather Engines
* **GET** `/api/locations` - Extracts a user's entire saved favorite cities portfolio map. *(Requires Authorization Header Bearer token)*.
* **POST** `/api/locations` - Saves a tracking city to the active user's document schema context (`city`, `country`). *(Requires Authorization Header Bearer token)*.
* **GET** `/api/weather/insights?city=London` - Triggers the core Express logic orchestration flow. Coordinates current weather variables with the `@google/genai` library module wrapper to return textual weather insights.
