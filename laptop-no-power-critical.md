# Incident: Laptop Not Powering On (Critical)

**Platform:** ServiceDesk Simulator
**Severity:** Critical
**Status:** Resolved

## Summary
A client emailed the IT department reporting that their work laptop would not turn on. The ticket was raised at critical severity because the client could not work.

## Troubleshooting
- The client had already tried a different power outlet and a different charging cable, with no change.
- With the outlet and cable ruled out, the fault was most likely in the laptop itself, and it couldn't be fixed remotely.

## Resolution
Because of the critical severity, I built a deployment for a replacement desktop so the client could keep working instead of waiting on a repair.

**Deployment method decision:** I compared imaging and cloud-based zero-touch deployment and chose **imaging**. It let me boot and fully set up the device before shipping, so it arrived ready to use. Zero-touch would have left the final configuration out of my hands. The tradeoff is more hands-on technician time, but I got more control and could verify the build before it left.

**Imaging steps**
1. Selected the device type: a desktop, not a PC/laptop build.
2. Connected the network cable, mouse, and keyboard.
3. Powered on the desktop and pressed F12 repeatedly during startup to reach the boot options.
4. Selected **PXE boot (IPv4)**, so the desktop booted over the network and pulled the image from the deployment server.
5. Entered the deployment credentials.
6. Assigned the desktop a unique ID (for example, SD2036) so it could be tracked as an asset.
7. Logged in with the user's username and password to confirm everything was set up correctly.
8. Shipped the verified desktop to the client.

## Outcome
The client received a working, pre-configured desktop and was back to work. Ticket closed.

## Takeaways
- Quick checks (outlet, cable) come first, but severity should drive how fast you move to a workaround.
- Choosing a deployment method means weighing speed against control. Here, control mattered more.
- Verifying the build before shipping avoids a second round of downtime for the client.
