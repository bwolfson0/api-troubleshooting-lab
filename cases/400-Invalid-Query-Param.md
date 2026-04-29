## Case: 400 Bad Request (Invalid Query Parameter)

**Issue**  
User receives a 400 Bad Request when attempting to retrieve users using a query parameter.

**Reproduction**  
Send a GET request to `/users` with an invalid `page` value:

GET http://localhost:3000/users?page=abc

**Observed Behavior**  
API returns a 400 Bad Request indicating that the `page` parameter must be a number.

**Expected Behavior**  
API should return user data when a valid numeric page value is provided.

**Analysis**  
The request reaches the correct endpoint, but fails validation due to an invalid query parameter type. This indicates the error occurs at the input validation stage before request processing.

**Root Cause**  
The `page` query parameter is provided as a string (`abc`), while the API expects a numeric value. This type mismatch causes validation to fail and results in a 400 response.

**Resolution**  
Ensure the `page` query parameter is a valid number greater than or equal to 1 (e.g., `page=2`).

**Example Response:**  

![400 Invalid Query Parameter](images/400-invalid-query.png)
