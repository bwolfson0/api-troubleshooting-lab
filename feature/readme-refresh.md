# API Troubleshooting Lab

A portfolio project demonstrating structured API troubleshooting and root cause analysis using **Postman** and a local **Node.js / Express** API.

This repository simulates real-world API support scenarios commonly encountered by Technical Support Engineers and Product Support Engineers. Each investigation follows a repeatable process to reproduce issues, collect evidence, identify the failure layer, determine the root cause, and document a resolution.

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

Every case follows the same structured troubleshooting workflow:

1. Reproduce the issue
2. Observe the behavior
3. Compare expected vs. actual results
4. Identify the failing layer
5. Analyze available evidence
6. Determine the root cause
7. Document the resolution

This mirrors the investigation process used by technical support teams when diagnosing customer issues.

---

# Scenario Coverage

## 400 Bad Request

- Invalid Query Parameter
- Unsupported HTTP Method

## 401 Unauthorized

- Missing API Key
- Invalid API Key

## 403 Forbidden

- Insufficient Permissions

## 404 Not Found

- Resource Does Not Exist
- Route Mismatch

## 429 Too Many Requests

- Rate Limiting

## 500 Internal Server Error

- Server Crash
- Dependency Failure

---

# Advanced Investigations

## Database Table Missing

A valid request reaches the correct endpoint but fails during server-side processing because the application references a database table that does not exist.

**Skills demonstrated**

- Log analysis
- Server-side troubleshooting
- Database failure identification
- Root cause documentation

---

## Incorrect Data Returned (200 OK)

A successful HTTP response returns unexpected data, demonstrating that a successful status code does not always indicate a successful outcome.

**Skills demonstrated**

- Response validation
- Data verification
- Functional troubleshooting

---

# Tools Used

## Postman

- API request construction
- Header validation
- Response inspection
- Environment testing

## Node.js & Express

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

This project demonstrates practical troubleshooting skills through realistic API support scenarios rather than algorithm exercises or CRUD applications.

The focus is on structured investigation, evidence-based analysis, and clear technical communication—the same skills used by Technical Support Engineers and Product Support Engineers when diagnosing customer issues.

---

# Future Investigation Ideas

- Browser DevTools Network Analysis
- HTTP 304 Cache Investigation
- CORS Troubleshooting
- Authentication Token Investigation
- HAR File Analysis
- API Performance Investigation
