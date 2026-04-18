# SOC Lab 3: Linux Authentication Log Analysis (Splunk Environment)

## Objective
The objective of this lab was to analyze Linux authentication logs and identify failed login attempts using system logs and Splunk concepts. The lab also focused on understanding authentication events, system user activity, and log interpretation within a SOC environment.

---

## Environment
- Ubuntu Linux VM
- Splunk Enterprise (log analysis platform)
- Authentication logs: `/var/log/auth.log`
- Shared folder export via VirtualBox (`vboxsf`)

---

## Methodology

1. Reviewed Linux authentication logs using command-line tools.
2. Inspected `/var/log/auth.log` for authentication-related events.
3. Generated controlled authentication activity using `su testuser`.
4. Attempted failed login simulation to observe log generation behavior.
5. Exported log samples to shared folder for evidence collection.
6. Prepared structured raw log dataset for SOC reporting.

---

## Key Observations

- The system recorded `su` session attempts and root-level activity.
- Cron and system processes generated normal authentication session logs.
- No persistent or repeated failed password attempts were found in the environment.
- Authentication logs primarily reflected normal system operations rather than malicious activity.

---

## Findings

- No evidence of brute-force attacks or repeated failed login attempts.
- Authentication logs indicate normal system behavior and administrative actions.
- Observed logs included:
  - Session open/close events for root
  - System-level authentication events (cron, sudo, su)

---

## Conclusion

The system is currently operating under normal authentication conditions with no signs of unauthorized access attempts or suspicious login activity.

This lab demonstrated how to:
- Access and interpret Linux authentication logs
- Identify system vs security-relevant events
- Understand how authentication data appears in raw log format
- Export evidence for SOC reporting purposes

---

## Skills Learned

- Linux log analysis basics
- Authentication event interpretation
- Differentiating system activity vs security events
- Evidence collection and export (VirtualBox shared folders)
- Basic SOC investigative workflow

---

## Outcome

Lab 3 is complete. The environment is now prepared for deeper SOC analysis using Splunk-based detection queries in future labs.