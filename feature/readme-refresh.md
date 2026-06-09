# API Troubleshooting Lab

A portfolio project demonstrating structured API troubleshooting and root cause analysis using **Postman** and a local **Node.js / Express** API.

This repository simulates realistic API support scenarios commonly encountered by Technical Support Engineers and Product Support Engineers. Each investigation follows a consistent process to reproduce an issue, collect evidence, identify the failure layer, determine the root cause, and document a resolution.

---

# Skills Demonstrated

- API troubleshooting
- HTTP request and response analysis
- Root cause investigation
- Authentication and authorization debugging
- Request validation
- Route verification
- Server-side error analysis
- Technical documentation
- Postman testing
- Problem reproduction and resolution

---

# Investigation Methodology

Each case follows a structured troubleshooting workflow:

1. Reproduce the issue
2. Observe the behavior
3. Compare expected vs. actual results
4. Identify the failing layer
5. Analyze available evidence
6. Determine the root cause
7. Document the resolution

This mirrors the investigation process used by technical support teams when diagnosing customer issues.

---

# Scenarios

### 400 Bad Request

- [Unsupported HTTP Method](cases/400-unsupported-http-method.md)
- [Invalid Query Parameter](cases/400-invalid-query-param.md)

### 401 Unauthorized

- [Invalid API Key](cases/401-invalid-api-key.md)
- [Missing API Key](cases/401-missing-api-key.md)

### 403 Forbidden

- [Insufficient Permissions](cases/403-insufficient-permission.md)

### 404 Not Found

- [Resource Does Not Exist](cases/404-resource-does-not-exist.md)
- [Route Mismatch](cases/404-route-mismatch.md)

### 429 Too Many Requests

- [Rate Limiting](cases/429-rate-limit.md)

### 500 Internal Server Error

- [Server Crash](cases/500-error.md)
- [Dependency Failure](cases/500-dependency-failure.md)

### Advanced Cases

- [Database Table Missing](advanced-cases/api-db/500-db-failure.md)
- [200 Incorrect Data Returned](advanced-cases/api-db/200-wrong-data.md)

---

# Tools Used

### Postman

- API request construction
- Header validation
- Response inspection
- Environment testing

### Node.js & Express

- Local API simulation
- Error reproduction
- Server-side debugging

---

# Example Investigation Workflow

```text
Customer reports issue
        ↓
Reproduce request
        ↓
Observe response
        ↓
Analyze evidence
        ↓ 
Identify root cause
        ↓
Document resolution
```

---

# Purpose

This project demonstrates structured troubleshooting, evidence-based analysis, and clear technical communication through realistic API support scenarios.

The goal is to practice the investigation process used by Technical Support Engineers and Product Support Engineers when diagnosing API issues and documenting solutions.
