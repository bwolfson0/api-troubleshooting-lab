## Case: 500 Internal Server Error (Dependency Failure)

**Issue**  
User reports that retrieving user details results in a 500 Internal Server Error for certain users.

**Reproduction**  
Send GET requests to the following endpoints:

GET http://localhost:3000/users-dep/1  
GET http://localhost:3000/users-dep/2  

Result:
- `/users-dep/1` → 200 OK  
- `/users-dep/2` → 500 Internal Server Error  

**Observed Behavior**  
API returns 200 OK for some user IDs and 500 Internal Server Error for others.

**Expected Behavior**  
API should consistently return complete user data for all valid users.

**Analysis**  
The request structure and authentication are valid, but the failure occurs only for specific users. This indicates a server-side issue triggered during request processing rather than a client or validation error.

**Root Cause**  
The API relies on a dependent service to fetch user profile data. For certain users, this dependency fails (e.g., service error), causing the request to throw an exception and return a 500 response.

**Resolution**  
Implement proper error handling and fallback logic when dependency calls fail. Additionally, investigate and stabilize the dependent service.

**Example Response:** 

![500 Dependency Error](../images/500-dependency.png)
