## TC-001: Successful login with valid credentials

Related scenario: TS-001  
Requirement: REQ-001

Preconditions:
- User has an active account.

Test data:
- Valid email
- Valid password

Steps:
1. Open login page.
2. Enter valid email.
3. Enter valid password.
4. Click "Log in".

Expected result:
- User is logged in.
- User is redirected to dashboard.

# TC-002: Login with invalid password

Related scenario: TS-002  
Requirement: REQ-002

Preconditions:
- User has an active account.

Test data:
- Valid email
- Invalid password

Steps:
1. Open login page.
2. Enter valid email.
3. Enter invalid password.
4. Click "Log in".

Expected result:
- User is not logged in.
- Error message is displayed.
- User remains on the login page.

# TC-005: Password reset link cannot be reused

Related scenario: TS-005  
Requirement: REQ-005

Preconditions:
- User has an active account.
- Password reset link has been generated.

Test data:
- Registered email
- Valid reset link
- New password

Steps:
1. Open password reset link.
2. Set a new password.
3. Confirm password change.
4. Open the same reset link again.
5. Try to set another password.

Expected result:
- Password is changed after first use of the reset link.
- The same reset link cannot be used again.
- System displays information that the link is expired or already used.
