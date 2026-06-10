# API Troubleshooting Lab

A portfolio project demonstrating structured API and browser troubleshooting using **Postman**, **Chrome DevTools**, and local **Node.js / Express** applications.

This repository contains reproducible investigations modeled after real Technical Support Engineer and Product Support Engineer workflows. Each investigation focuses on reproducing an issue, collecting evidence, identifying the root cause, documenting a resolution, and verifying the result.

---

# Skills Demonstrated

- API troubleshooting
- Browser network analysis
- HTTP request and response inspection
- Root cause investigation
- Authentication and authorization debugging
- Browser cache investigation
- CORS troubleshooting
- Request validation
- Route verification
- Server-side error analysis
- Technical documentation
- Postman testing
- Chrome DevTools
- Problem reproduction and verification

---

# Investigation Methodology

Every investigation follows the same structured workflow:

1. Reproduce the issue
2. Observe the behavior
3. Collect evidence
4. Analyze findings
5. Determine the root cause
6. Implement or recommend a resolution
7. Verify the result

This mirrors the investigation process commonly used by Technical Support and Product Support teams when diagnosing customer issues.

---

# API Investigations

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

---

# Advanced API Investigations

- [Database Table Missing](advanced-cases/api-db/500-db-failure.md)
- [200 Incorrect Data Returned](advanced-cases/api-db/200-wrong-data.md)

---

# Browser Investigations

- [HTTP 304 Not Modified](browser-investigations/304-not-modified.md)
- [CORS Policy Blocking API Request](browser-investigations/cors-request-blocked.md)

---

# Tools Used

### Postman

- API request construction
- Header validation
- Response inspection
- Environment testing

### Chrome DevTools

- Browser Console
- Network analysis
- Request and response inspection
- Header analysis

### Node.js & Express

- Local API simulation
- Browser integration testing
- Error reproduction

---

# Investigation Workflow

```text
Customer Report
      ↓
  Reproduce
      ↓
   Observe
      ↓
Collect Evidence
      ↓
   Analyze
      ↓
  Root Cause
      ↓
  Resolution
      ↓
 Verification
```

---

# Purpose

This project demonstrates structured troubleshooting, evidence-based analysis, and clear technical communication through realistic API and browser support scenarios.

The focus is on developing the investigation process used by Technical Support Engineers and Product Support Engineers when diagnosing API integrations, browser behavior, authentication issues, and server responses.

````
