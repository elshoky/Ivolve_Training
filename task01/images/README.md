# README: Create Group, User, Assign Permissions, and Install Nginx

This guide explains how to:
1. Create a new group `ivolve`.
2. Create a new user `luffy` and assign the user to the `ivolve` group.
    ![alt text](Ivolve_Training/task01/images/1.jpg)
3. Grant the user `luffy` permission to install Nginx with elevated privileges without a password prompt.
   ![alt text](Ivolve_Training/task01/images/2.jpg)
5. Install Nginx using the `luffy` user.
   ![alt text](Ivolve_Training/task01/images/3.jpg)
6.  Check of install nginx
   ![alt text](Ivolve_Training/task01/images/4.jpg)
7. Try to install httpd
   ![alt text](Ivolve_Training/task01/images/5.jpg)
## Step 1: Create the Group `ivolve`

First, create a new group named `ivolve`. Run the following command as the root user:

```bash
groupadd ivolve
useradd -m -G ivolve luffy
passwd luffy
visudo
luffy ALL=(ALL) NOPASSWD: /usr/bin/apt-get install nginx
su - luffy
apt-get install nginx
