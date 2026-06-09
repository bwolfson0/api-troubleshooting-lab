# Browser Investigation: HTTP 304 Not Modified

## Overview

This investigation examines an **HTTP 304 Not Modified** response captured in Chrome DevTools while accessing `https://www.example.com/`.

The objective is to understand why the browser receives a **304 Not Modified** response instead of **200 OK** and document the investigation process using browser network data and HTTP headers.

---

## Issue

Refreshing the page returns **304 Not Modified** instead of **200 OK**, raising the question of whether the browser is requesting outdated content or the server is behaving unexpectedly.

---

## Environment

| Property | Value |
|------------|------------|
| Browser | Google Chrome |
| Tool | Chrome DevTools - Network Tab |
| Request Method | GET |
| URL | https://www.example.com/ |

---

## Reproduction

1. Open Chrome DevTools.
2. Navigate to the **Network** tab.
3. Enable **Preserve log**.
4. Leave **Disable cache** unchecked.
5. Refresh the page multiple times.
6. Select the request returning **304 Not Modified**.

---

## Observed Behavior

The browser sends a **GET** request and receives the following response:

```
Status Code: 304 Not Modified
```

No response body is returned because the browser already has a cached copy of the resource.

---

## Expected Behavior

If the resource has changed, the server should return:

```
200 OK
```

and provide an updated response body.

If the resource has not changed, the server may return:

```
304 Not Modified
```

allowing the browser to reuse its cached copy.

---

## Evidence Collected

### General

| Property | Value |
|------------|------------|
| Request URL | https://www.example.com/ |
| Request Method | GET |
| Status Code | 304 Not Modified |

### Request Headers

| Header | Value |
|------------|------------|
| Cache-Control | max-age=0 |
| If-Modified-Since | Tue, 09 Jun 2026 16:58:07 GMT |

### Response Headers

| Header | Value |
|------------|------------|
| ETag | "6a28461f-22f" |
| Last-Modified | Tue, 09 Jun 2026 16:58:07 GMT |

---

## Analysis

The browser includes an **If-Modified-Since** header containing the timestamp of its cached resource.

The server compares this value with the current version of the resource and determines that no changes have occurred since that timestamp.

Instead of transmitting the resource again, the server returns **304 Not Modified**, allowing the browser to continue using its cached copy.

The matching **If-Modified-Since** and **Last-Modified** values support this conclusion.

---

## Root Cause

No application or server error was identified.

The response is the result of successful HTTP cache validation between the browser and the server.

---

## Resolution

No corrective action is required.

The observed behavior is expected and indicates that browser caching is functioning correctly.

If updated content is required, performing a hard refresh or clearing the browser cache will force retrieval of a new copy of the resource.

---

## Support Engineer Skills Demonstrated

- Chrome DevTools
- Browser Network Analysis
- HTTP Request and Response Inspection
- Header Analysis
- Browser Cache Investigation
- Root Cause Analysis
- Technical Documentation

---

## Screenshots

### Network Request

![304 Network Request](images/304-network-overview.png)

### Request and Response Headers

![304 Headers](images/304-headers.png)
