# BUG-001: Password reset link can be reused after successful password change

Related test case: TC-005  
Related requirement: REQ-005

Environment: Test  
Build: AUTH-MODULE-1.0.0

Steps to reproduce:
1. Request password reset for a registered user.
2. Open reset link from email.
3. Set a new password.
4. Log in successfully with the new password.
5. Open the same reset link again.
6. Set another new password.

Expected result:
The reset link should be invalid after first successful use.

Actual result:
The same reset link can be reused to change the password again.

Severity: High  
Priority: High

Impact:
This creates a security risk because a previously used reset link remains valid.

Recommendation:
Invalidate reset token immediately after successful password change and add regression coverage for reset token reuse.

# BUG-002: Password reset message reveals whether email exists

Related test case: TC-006  
Related requirement: REQ-006

Environment: Test  
Build: AUTH-MODULE-1.0.0

Steps to reproduce:
1. Open password reset page.
2. Enter non-existing email address.
3. Submit password reset request.
4. Repeat the same action with a registered email address.
5. Compare displayed messages.

Expected result:
The system should display a generic message in both cases, for example: "If the email exists, password reset instructions will be sent."

Actual result:
The system displays different messages for registered and non-existing emails.

Severity: Medium  
Priority: High

Impact:
This behavior may allow user enumeration.
