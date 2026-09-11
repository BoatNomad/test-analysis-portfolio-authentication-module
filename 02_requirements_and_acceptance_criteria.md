# REQ-002: Login with invalid password

User should not be able to log in with an invalid password.

## Acceptance Criteria

AC-002: Given the user has an active account, when the user enters a valid email and invalid password, then the system rejects the login attempt and displays an error message.


# REQ-003: Password reset request

User should be able to request a password reset link using a registered email address.

## Acceptance Criteria

AC-003: Given the user has an active account, when the user requests a password reset, then the system sends a password reset link to the registered email address.


# REQ-004: Expired reset link

Password reset link should not be valid after expiration time.

## Acceptance Criteria

AC-004: Given the reset link has expired, when the user opens the link, then the system rejects the request and displays information that the link is expired.


# REQ-005: One-time reset link

Password reset link should be valid only once.

## Acceptance Criteria

AC-005: Given the user has already used a password reset link, when the user opens the same link again, then the system rejects the link as already used.
