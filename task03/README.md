# Ping Server Script

This script pings all the servers in the subnet `192.168.116.x` (where `x` is a number between 1 and 254) and logs the results into two files:
- **reachable_servers.txt**: Servers that responded successfully to the ping.
- **unreachable_servers.txt**: Servers that did not respond to the ping.

## Prerequisites

Ensure that your system has:
- A working network connection.
- Bash installed (the script is written in Bash).
- Proper permissions to write to the directory where the log files will be stored.

## Steps to Use the Script

1. **Clone the Repository or Download the Script**  
   Clone the repository or download the script to your local machine.
	
	![Create Group and User](script.JPG)
	
2. **Set the Target Directories**  
   The script saves the results of the ping test into the following files:
   - `reachable_servers.txt`
   - `unreachable_servers.txt`

   These files will be created in the following directory:  
   `~elshoky/Ivolve_training/task03/`

   If the directories do not exist, the script will create them automatically.

3. **Make the Script Executable**  
   After downloading or cloning the script, navigate to the directory containing the script, and then run the following command to make it executable:
   ```bash
   chmod +x ping_servers.sh

	![Create Group and User](3.JPG)

4. **Run the Script
   ./ping_servers.sh

	        ![Create Group and User](4.JPG)

5. **Check the Results

   cat ~elshoky/Ivolve_training/task03/reachable_servers.txt
   cat ~elshoky/Ivolve_training/task03/unreachable_servers.txt

	        ![List-Files](5.JPG)
		![Show-Reachable&UnreachableFiles ](6.JPG)


### Instructions:

1. **Save the above content as `README.md`** in the root of your project.
2. **Ensure the paths** (e.g., `~/Ivolve_training/task03/`) are correct and accessible.
3. **Commit and push the `README.md`** file to your GitHub repository.

This `README.md` will help other users understand the process and quickly set up and run the script. Let me know if you'd like to make any changes or additions!

