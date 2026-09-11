## SQL
```sql
SELECT *
FROM users
WHERE email = 'active.user@example.com';
```

## Verify failed login attempts

```sql
SELECT id, email, failed_login_attempts
FROM users
WHERE email = 'active.user@example.com';
```


## Verify password reset token status

```sql
SELECT user_id, token, used, expires_at
FROM password_reset_tokens
WHERE user_id = 123
ORDER BY created_at DESC;
```


### REST API TESTING
POST /api/login

Expected status:
200 OK

Expected response:
- auth token is returned
- user id is returned


### CHROME DEVTOOLS
In Chrome DevTools, Network tab can be used to verify:
- request URL
- HTTP method
- status code
- request payload
- response body
