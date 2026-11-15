# Task: New User Account Setup in Active Directory

**Platform:** ServiceDesk Simulator
**Severity:** Medium
**Status:** Resolved

## Summary
A ticket requested a new user ID for an employee, with access appropriate to their job.

## Resolution
Using Active Directory, I:
1. Created the new user account and user ID.
2. Assigned the user to their department.
3. Assigned their role.
4. Granted access to only the resources needed to perform their duties, following the principle of least privilege.

## Outcome
The employee had a working account with the access needed for their job and nothing beyond it. Ticket closed.

## Security Note
Least privilege means giving users only the access they need. This limits the damage if an account is ever compromised and reduces the chance of accidental access to sensitive data.

## Takeaways
- Setting up access correctly at account creation is easier than cleaning up excess permissions later.
