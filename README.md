# API Troubleshooting Lab

This project simulates real-world API issues and demonstrates structured troubleshooting techniques using Postman and a local Node.js API.

---

## Scenarios Covered

- **400** — Validation / bad input  
- **401** — Authentication failures  
- **403** — Authorization / permission issues  
- **404** — Routing and missing resources  
- **500** — Server and dependency failures  
- **429** — Rate limiting  

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

**Reproduction**  
GET /users?page=2  
Header: `x-api-key: wrongkey`

**Observed Behavior**  
401 Unauthorized

**Root Cause**  
Invalid API key causes authentication failure.

**Resolution**  
Provide a valid API key in the request headers.

---

## Scenarios

### 400 Bad Request
- [Unsupported HTTP Method](cases/400-Unsupported-HTTP-Method.md)  
- [Invalid Query Parameter](cases/400-Invalid-Query-Param.md)  

### 401 Unauthorized
- [Invalid API Key](cases/401-Invalid-API-Key.md)  
- [Missing API Key](cases/401-Missing-API-Key.md)  

### 403 Forbidden
- [Insufficient Permissions](cases/403-Insufficient-Permission.md)  

### 404 Not Found
- [Resource Does Not Exist](cases/404-Resource-Does-Not-Exist.md)  
- [Route Mismatch](cases/404-Route-Mismatch.md)  

### 500 Internal Server Error
- [Server Crash](cases/500-Error.md)  
- [Dependency Failure](cases/500-Dependency-Failure.md)  

### 429 Too Many Requests
- [Rate Limiting](cases/429-rate-limit.md)  

---

## Tools Used

- Postman (API testing)  
- Node.js (local API simulation)  
- Express (server framework)  

---

## Purpose

This project demonstrates the ability to diagnose API issues, identify root causes, and clearly communicate resolutions—core skills for technical support and support engineering roles.
