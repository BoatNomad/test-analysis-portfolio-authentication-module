## BUG-001: Password reset link can be reused

Related test case: TC-007

Environment:
Test

Steps to reproduce:
1. Request password reset.
2. Open reset link.
3. Set a new password.
4. Open the same reset link again.
5. Set another password.

Expected result:
The reset link should be invalid after first use.

Actual result:
The reset link can be reused.

Severity:
High

Priority:
High
