# Test Summary Report

## Scope

Authentication module:
- login
- invalid login attempts
- password reset request
- expired reset link
- reset link reuse
- basic security-related checks

## Test execution summary

| Status | Count |
|---|---:|
| Passed | 5 |
| Failed | 2 |
| Blocked | 0 |
| Total | 7 |

## Main risks

- Password reset link can be reused after successful password change.
- Password reset flow reveals whether an email exists.
- Missing or unclear requirements for account lockout and reset link expiration time.

## Recommendation

Release is not recommended until BUG-001 is fixed and retested.

BUG-002 should be reviewed with Product Owner/security/business team because it may create user enumeration risk.
