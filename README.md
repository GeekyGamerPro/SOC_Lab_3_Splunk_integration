# SOC_Lab_3_Splunk_integration
SOC Lab 3 focused on deploying and troubleshooting a local SIEM using Splunk Enterprise in an Ubuntu VM. Tasks included resolving startup issues, fixing authentication errors, and restoring web access to enable basic log analysis readiness.
📄 SOC Lab – Splunk Setup & Log Analysis (Day 3)
🧠 Overview

This lab focused on setting up and troubleshooting a local SIEM environment using Splunk Enterprise inside an Ubuntu virtual machine. The objective was to simulate a SOC analyst workflow: environment setup, service troubleshooting, authentication recovery, and log access.

🖥️ Environment
OS: Ubuntu (VirtualBox VM)
SIEM Tool: Splunk Enterprise (Local Install)
Access: http://localhost:8000
Host Machine: macOS
⚠️ Issues Encountered

During setup and usage, multiple issues occurred:

Splunk web interface failed to consistently start
“Waiting for web server at 127.0.0.1:8000” hang state
Permission errors related to splunk.pid file
Splunk service appearing frozen during startup
Admin login repeatedly failing despite password resets
Authentication state becoming inconsistent across restarts
🔧 Troubleshooting Steps Taken

The following remediation steps were performed:

Verified Splunk process state using:
ps aux | grep splunk
Terminated stuck Splunk processes:
pkill -f splunk
Restarted Splunk in foreground and background modes
Resolved PID lock issues causing startup conflicts
Attempted CLI password resets for admin user
Cleared authentication state inconsistencies
Rebuilt admin credentials using user-seed.conf
Performed clean restart of Splunk service
🔐 Final Resolution

The issue was resolved by:

Resetting Splunk authentication using user-seed.conf
Restarting Splunk cleanly
Successfully reinitializing the admin account

Login access was restored:

Username: admin
Password: Password123!
📊 Outcome
Splunk web interface successfully loaded at http://localhost:8000
Admin access restored
SIEM environment fully operational
Ready for log ingestion and SOC analysis exercises
📸 Evidence

Screenshots included:

Splunk login page
Splunk dashboard home
Terminal outputs during recovery process
🧠 Key Learning Takeaways
SIEM tools require stable service states to function correctly
Authentication issues are often caused by corrupted or unsynced config states
CLI troubleshooting is critical in SOC environments
VM-based lab environments can introduce service instability
Proper recovery procedures are more valuable than repeated resets
🚀 Next Steps
Ingest system logs into Splunk
Perform failed login detection queries
Build basic SOC dashboards
Simulate attack detection scenarios
