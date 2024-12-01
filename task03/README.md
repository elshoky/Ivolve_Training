Ping Server Script
This script pings all the servers in the subnet 192.168.116.x (where x is a number between 1 and 254) and logs the results into two files:

reachable_servers.txt: Servers that responded successfully to the ping.
unreachable_servers.txt: Servers that did not respond to the ping.
Prerequisites
Ensure that your system has:

A working network connection.
Bash installed (the script is written in Bash).
Proper permissions to write to the directory where the log files will be stored.
Steps to Use the Script
1. Clone the Repository or Download the Script
Clone the repository or download the script to your local machine.



2. Set the Target Directories
The script saves the results of the ping test into the following files:

reachable_servers.txt
unreachable_servers.txt
These files will be created in the following directory:
~/Ivolve_training/task03/

If the directories do not exist, the script will create them automatically.

3. Make the Script Executable
After downloading or cloning the script, navigate to the directory containing the script, and then run the following command to make it executable:

bash
Copy code
chmod +x ping_servers.sh

4. Run the Script
Execute the script using the following command:

bash
Copy code
./ping_servers.sh

5. Check the Results
After running the script, check the results in the output files:

reachable_servers.txt: Contains servers that responded successfully to the ping.
unreachable_servers.txt: Contains servers that did not respond to the ping.
To view the results, use the following commands:

bash
Copy code
cat ~/Ivolve_training/task03/reachable_servers.txt
cat ~/Ivolve_training/task03/unreachable_servers.txt


Additional Notes
The script ensures directories and files are created automatically if they do not exist.
It uses simple bash scripting to perform sequential pings across the specified subnet.
To automate the execution of this script, consider scheduling it with cron.
Steps to Push the README.md to GitHub
Save this file as README.md in the root of your project directory.
Run the following commands to push the file to your GitHub repository:
bash
Copy code
git add README.md
git commit -m "Added README.md for ping script task"
git push origin main
