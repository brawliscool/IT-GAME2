# IT Desk Simulator

A browser-based desktop support simulation game. You work a realistic service-desk queue, remote into employee workstations, diagnose the actual fault, apply a fix, verify the result, and close the incident.

## Current playable build

- Mobile-first dark service-desk UI
- Persistent shift progress with `localStorage`
- Ticket priorities, SLA context, users, departments, endpoints, and support chat
- Simulated remote Windows workstation
- Interactive Command Prompt with contextual commands
- Network settings / DNS troubleshooting
- Task Manager / high-CPU troubleshooting
- Windows Services / Print Spooler troubleshooting
- Device Manager / display adapter troubleshooting
- Account administration / lockout troubleshooting
- Fix verification instead of instant success buttons
- XP, rating, credits, resolution quality, and performance history
- Built-in knowledge base

## Included incidents

1. Connected to Wi-Fi but DNS is misconfigured
2. Print queue stuck because Print Spooler is stopped
3. Laptop slow because a Teams updater process is consuming CPU
4. User account locked after failed password attempts
5. External display missing because the display adapter is disabled

## Run locally

No build system or dependencies are required. Serve the repository with any static web server, or open `index.html` directly in a modern browser.

Example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Gameplay loop

1. Select a ticket.
2. Read the symptoms and talk to the user if useful.
3. Accept the incident and connect remotely.
4. Inspect the simulated workstation with the appropriate tools.
5. Apply the correct fix.
6. Run verification.
7. Return to the ticket and close it.

Unnecessary actions and failed verification attempts reduce performance. Efficient, correct troubleshooting produces higher resolution scores and more XP.

## Next expansion targets

- More randomized incident variants
- Active Directory and Microsoft 365 admin consoles
- Event Viewer and registry simulation
- VPN, Outlook, BitLocker, malware, permissions, storage, and update incidents
- Shift events and company-wide outages
- Career levels, certifications, unlocks, and salaries
- More realistic customer conversations
- Scenario authoring system
