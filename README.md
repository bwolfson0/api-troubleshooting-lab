# api-troubleshooting-lab
Simulated API troubleshooting scenarios (400, 401, 403, 404, 500, 429) using Postman and a local Node.js API

# API Troubleshooting Lab
This project simulates real-world API issues and demonstrates structured troubleshooting techniques.

Scenarios include:
- 400 (validation errors)
- 401 / 403 (authentication & authorization)
- 404 (routing and missing resources)
- 500 (server and dependency failures)
- 429 (rate limiting)

## Debugging Approach
1. Reproduce the issue
2. Compare working vs failing requests
3. Identify failure layer:
   - Input
   - Authentication
   - Authorization
   - Routing
   - Processing
   - Dependency
4. Determine root cause
5. Propose resolution

## Example: 401 Unauthorized (Invalid API Key)

**Issue:**  
User receives 401 Unauthorized when accessing endpoint.

**Reproduction:**  
GET /users?page=2  
Header: x-api-key: wrongkey

**Observed:**  
401 Unauthorized

**Root Cause:**  
Invalid API key causes authentication failure.

**Resolution:**  
Use a valid API key in request headers.

## Scenarios

- [400 Validation Errors](cases/400-validation.md)
- [401 Authentication](cases/401-auth.md)
- [403 Authorization](cases/403-permissions.md)
- [404 Not Found](cases/404-routing.md)
- [500 Server Errors](cases/500-errors.md)
- [429 Rate Limiting](cases/429-rate-limit.md)
