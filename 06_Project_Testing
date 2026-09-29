# Phase 6: Project Testing

## 1. Postman Test Strategy & Assertion Matrix
To verify that the AI WeatherWise endpoint endpoints are protected and functional, the API was tested using the Postman toolkit suite.

| Endpoint Route | HTTP Method | Expected Status | Validation Focus / Assertions |
| :--- | :--- | :--- | :--- |
| `/api/auth/register` | POST | `201 Created` | Confirms user profile schema creation and bcrypt password hashing. |
| `/api/auth/login` | POST | `200 OK` | Verifies credentials and returns a valid signed JWT bearer token. |
| `/api/locations` | GET | `401 Unauthorized` | Asserts that paths are completely guarded if no token is provided. |
| `/api/locations` | POST | `201 Created` | Validates creation of a favorite city under an authenticated profile context. |
| `/api/weather/insights`| GET | `200 OK` | Verifies third-party connectivity and checks for a valid Google Gemini summary response. |

---

## 2. Validation & Security Sanity Checks
* **Payload Sanitation:** Attempted injection payloads (XSS script injections and NoSQL parameters) were passed through Postman route parameters. The sanitization middleware successfully neutralized them.
* **Fallback Validation Mode:** Simulating server runtimes with the `GEMINI_API_KEY` environmental parameter removed successfully forced the server into its static fallback loop without throwing system errors or crashes.
