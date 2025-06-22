# Windows-Recon-Tool-kit
Description: The Windows Recon Toolkit is an advanced, automated reconnaissance payload designed for use with the o.mg cable or compatible HID injection devices. Once executed on a Windows 10 or 11 machine, it rapidly collects a comprehensive snapshot of system and user security information for red team or audit purposes.

Features:

Credential Harvesting:
Extracts saved Wi-Fi network names and their cleartext passwords for all profiles on the system.

System & User Audit:
Gathers detailed system information, computer specs, current user and group memberships, and active processes.

Software & Patch Status:
Lists installed software, running processes, open network ports, and applied system updates to help identify outdated software or vulnerabilities.

Privilege Escalation Checks:
Evaluates the machine for common privilege escalation vectors, including:

Admin rights status

UAC policy and AlwaysInstallElevated registry settings

Unquoted service paths

Writable service binaries

Weak scheduled tasks

Writable user registry keys

WSUS hijack vectors

AV/EDR (Antivirus/Endpoint Detection) products installed


Clipboard & Screenshot Capture:
Dumps the current clipboard content and takes a live screenshot of the user’s desktop environment.

Automated Exfiltration:
All gathered artifacts (recon report, clipboard, and screenshot) are uploaded directly to a Dropbox account via the API, using a supplied OAuth token for secure and rapid exfiltration.

Stealth & Cleanup:
Cleans up all temporary files and clears PowerShell command history to reduce forensic evidence of the operation.


Usage:
Deploy the Ducky Script on a Windows target. Within minutes, all key recon and credential data is exfiltrated to Dropbox, while traces are scrubbed from the system.

> Note: Replace "your_dropbox_url" with your Dropbox API token before deployment. Only use on systems you own or have explicit permission to test.
