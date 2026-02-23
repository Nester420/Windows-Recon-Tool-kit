This payload is a BadUSB (Ducky Script) Windows Recon Toolkit that automates full system reconnaissance on a target Windows machine using PowerShell, and exfiltrates the data to a Dropbox account.


---

🔧 How It Works

The payload performs the following steps:

🧠 1. Launch PowerShell

GUI r → STRING powershell → ENTER

📁 2. Define Temporary Paths

Creates three temp files:

recon_report.txt (system info)

clipboard.txt (clipboard dump)

screenshot.jpg (screen capture)


📡 3. Reconnaissance Collection

Data gathered includes:

Saved Wi-Fi credentials (SSID + password)

System info

Installed programs

Top processes by CPU usage

Open network ports (netstat)

Missing patches (Get-HotFix)

Privilege escalation checks, including:

Admin rights

UAC settings

Weak scheduled tasks

Writable registry keys

WSUS hijack info

AV/EDR detection



📋 4. Clipboard Dump

Saves the current clipboard contents.

☁️ 5. Dropbox Upload

Uploads all three files to the attacker's Dropbox account using the Dropbox API and a personal token:

$token = "your_drop_box_token"

You must replace this with your own Dropbox API token.

🧹 7. Cleanup

Deletes recon files and screenshot

Clears PowerShell history


❌ 8. Exit

Closes PowerShell to hide tracks.


---

🚀 How to Use

1. Replace Token:

Update the line STRING $token = "your_drop_box_token" with your Dropbox API bearer token.



2. place the Payload:

Use a BadUSB device (e.g., Rubber Ducky, OMG Cable) if used on a rubber ducky use hak5s payload studio to convert the payload into a .bin file name it inject.bin and place it on the root directory of the rubber ducky. if useing with the omg cable simply place the payload in one of the payload slots and execute the payload. 



3. Deploy:

Plug into a target Windows machine.

Within ~20–30 seconds, all recon data will be uploaded to your Dropbox silently.





---


⚠️ Warning. this is to be used for educational purposes only. I am not liable for any damages nor legal trouble. only use on target machines with explicit permission or in a lab environment. again I am not liable for any damages. 


IF YOU ENJOY THIS PAYLOAD AS MUCH AS I HAVE PLEASE GIVE THIS REPO A STARE. 
