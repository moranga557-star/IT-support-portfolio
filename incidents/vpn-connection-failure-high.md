# Incident: VPN Connection Failure for Remote Worker

**Platform:** ServiceDesk Simulator
**Severity:** High
**Status:** Resolved

## Summary
A remote worker could not connect to the company VPN and raised a ticket with IT. The ticket was marked high severity because the worker couldn't reach company resources while working remotely.

## Troubleshooting and Resolution
1. Connected remotely to the worker's desktop.
2. Opened the terminal and ran `ipconfig /flushdns` to clear the DNS resolver cache. A stale or corrupted DNS cache can stop a client from resolving the VPN server's address correctly.
3. Restarted the computer to clear any lingering network state.
4. Had the worker sign in and reconnected the VPN.
5. Confirmed the VPN connection was established.

## Outcome
The worker's VPN connection was restored and he was able to work remotely again. Ticket closed.

## Security Note
In this case the simulator had me ask the worker for his password to sign in. In a real environment, I would have the worker enter his credentials himself while I watched through the remote session, so IT never sees or handles user passwords.

## Takeaways
- Flushing the DNS cache is a quick, low-risk first step for connectivity problems.
- Credentials should stay with the user, even during remote support.
