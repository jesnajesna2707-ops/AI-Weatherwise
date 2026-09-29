# Phase 3: Project Design

## 1. System Architecture (MVC Pattern)
The AI WeatherWise backend application strictly follows the Model-View-Controller (MVC) software design pattern to isolate data structures from business rules:
* **Model Layer:** Uses Mongoose schemas to map structure rules explicitly into MongoDB collections.
* **Controller Layer:** Captures application endpoints, checks incoming routing parameters, communicates with databases, and coordinates AI engines.
* **View Layer (API Routing Interface):** Since this is a pure headless backend API platform, the view layer consists of Express API endpoints returning structured JSON data.

---

## 2. Database Schema Configuration (Mongoose Layout)

### 2.1 User Entity Schema
```javascript
const userSchema = new mongoose.Schema({
  name: { type: String, required: true },
  email: { type: String, required: true, unique: true },
  password: { type: String, required: true },
  role: { type: String, default: "reader" }
}, { timestamps: true });
```

### 2.2 Location Entity Schema
```javascript
const locationSchema = new mongoose.Schema({
  user: { type: mongoose.Schema.Types.ObjectId, ref: 'User', required: true },
  city: { type: String, required: true },
  country: { type: String, required: true }
}, { timestamps: true });
```

---

## 3. Core Component Integrations
* **Express Gateway Server:** Binds system network environments and executes middleware parameters (CORS, body-parser, JSON sanitizers).
* **JWT Guard Middleware:** Intercepts secure header segments to validate security keys before resolving protected endpoints.
* **AI Orchestration Framework:** Feeds live meteorological data into the `@google/genai` framework to output natural language weather evaluations.
