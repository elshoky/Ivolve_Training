
# README: Create Group, User, Assign Permissions, and Install Nginx

This guide explains how to:
1. Create a new group called `ivolve`.
2. Create a new user named `luffy` and assign the user to the `ivolve` group.
    ![Create Group and User](Ivolve_Training/task01/images/1.jpg)
3. Grant the user `luffy` the necessary permissions to install Nginx with elevated privileges without requiring a password.
    ![Grant Permissions](Ivolve_Training/task01/images/2.jpg)
4. Install Nginx using the `luffy` user.
    ![Install Nginx](Ivolve_Training/task01/images/3.jpg)
5. Verify Nginx installation.
    ![Verify Installation](Ivolve_Training/task01/images/4.jpg)
6. Test the ability to install `httpd` (verify the sudo permission restriction).
    ![Test Permissions](Ivolve_Training/task01/images/5.jpg)

---

## Step 1: Create the Group `ivolve`

Start by creating a new group named `ivolve`. This group will be used to assign the user `luffy`:

```bash
groupadd ivolve
useradd -m -G ivolve luffy
passwd luffy
visudo
luffy ALL=(ALL) NOPASSWD: /usr/bin/apt-get install nginx
su - luffy
apt-get update
apt-get install nginx
