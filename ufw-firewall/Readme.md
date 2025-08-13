 Task 2: Basic Firewall Configuration using UFW

Objective
In this task, I set up a simple firewall on Ubuntu using UFW. The goal was to:
-  Allow SSH connections (port 22)
-  Block HTTP traffic (port 80)

Tools Used
- Ubuntu 22.04 LTS (via WSL2 on Windows)
- UFW (Uncomplicated Firewall)

What I Did
Here is  a quick breakdown of what I did:

1. Installed UFW with `sudo apt install ufw`
2. Allowed SSH: `sudo ufw allow ssh`
3. Denied HTTP: `sudo ufw deny http`
4. Enabled the firewall: `sudo ufw enable`
5. Checked the current rules with `sudo ufw status verbose`

 Final Firewall Status
SSH (port 22) is allowed, and HTTP (port 80) is blocked.  
I have included a screenshot below showing the rules in effect.

 Screenshot
_You can find the firewall status screenshot in this repo:_

 Files in This Repo
- `ufw_configuration.sh` : Shell script that runs all the firewall commands automatically
- `README.md`: You're reading it now
- `ufw_status_screenshot.png` : Screenshot showing the firewall is active

 Demo Video
You can find the firewall status video in this repo:

 Note
UFW does not always behave perfectly on WSL2 since it is not a full Linux kernel setup but in this case, the configuration and rules worked fine. On a real server or VM, UFW is more reliable for production use.
