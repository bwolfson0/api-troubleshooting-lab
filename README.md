# API Troubleshooting Lab

This project simulates real-world API issues and demonstrates structured troubleshooting techniques using Postman and a local Node.js API.

## Scenarios Covered

- 400 — Validation / bad input
- 401 — Authentication failures
- 403 — Authorization / permission issues
- 404 — Routing and missing resources
- 500 — Server and dependency failures
- 429 — Rate limiting

---

## Debugging Approach

1. Reproduce the issue  
2. Compare working vs failing requests  
3. Identify the failure layer:
   - Input (400)
   - Authentication (401)
   - Authorization (403)
   - Routing (404)
   - Processing / Server (500)
   - System limits (429)
4. Determine root cause  
5. Propose resolution  

---

## Example Case

### 401 Unauthorized (Invalid API Key)

**Issue**  
User receives 401 Unauthorized when accessing an endpoint.

**Reproduction**  
GET /users?page=2  
Header: x-api-key: wrongkey

**Observed Behavior**  
401 Unauthorized response returned

**Root Cause**  
Invalid API key causes authentication failure

**Resolution**  
Provide a valid API key in the request headers

---

## Scenarios

- [400 Validation Errors](cases/400-validation.md)
- [401 Authentication](cases/401-auth.md)
- [403 Authorization](cases/403-permissions.md)
- [404 Not Found](cases/404-routing.md)
- [500 Server Error](cases/500-error.md)
- [500 Dependency Error](cases/500-Dependency-Failure)
- [429 Rate Limiting](cases/429-rate-limit.md)

---

## Tools Used

- Postman (API testing)
- Node.js (local API simulation)
- Express (server framework)

---

## Purpose

This project demonstrates the ability to diagnose API issues, identify root causes, and clearly communicate resolutions—core skills for technical support and support engineering roles.
