# Disk Space Check and Alert Script

This script automates the process of checking the disk space usage of the root filesystem (`/`) on an Ubuntu server. If the disk usage exceeds a specified threshold (90%), the script sends an email alert to notify the user.

## Prerequisites

Before running this script, you need to have the following installed:

1. **msmtp**: A lightweight SMTP client used to send emails.
2. **Cron**: A job scheduler that runs the script at a specified time.

## Installation

### 1. Install msmtp

```bash
sudo apt update
sudo apt install msmtp msmtp-mta

### 2.  Create the Disk Usage Check Script

nano ~/check_disk_usage.sh

chmod +x ~/check_disk_usage.sh

### 4. Schedule the Script with Cron

crontab -e
0 17 * * * /home/elshoky/Ivolve_training/task02/check_disk_usage

### 5. How It Works

The script checks the disk usage of the root filesystem (/).
If the disk usage exceeds 90%, the script sends an email to the configured address (elshoky.360@gmail.com) using msmtp.
You can modify the threshold in the script if you want a different alert threshold

### 6. Customization

Email Address: Change the email address in the script to receive alerts at a different address.
Threshold: You can change the threshold percentage to a value of your choice (e.g., 80% or 95%).


### Final Steps
- Save the file by pressing `Ctrl + O`, then exit with `Ctrl + X`.
- The README provides a complete guide to set up, configure, and use the disk space alert script.

Let me know if you need any further edits or details!

