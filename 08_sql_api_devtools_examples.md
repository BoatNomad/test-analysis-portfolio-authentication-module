###SQL
SELECT *
FROM users
WHERE email = 'active.user@example.com';





###REST API TESTING
POST /api/login

Expected status:
200 OK

Expected response:
- auth token is returned
- user id is returned


###CHROME DEVTOOLS
In Chrome DevTools, Network tab can be used to verify:
- request URL
- HTTP method
- status code
- request payload
- response body
