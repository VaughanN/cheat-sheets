# CentOS

CentOS, from Community Enterprise Operating System; also known as CentOS Linux) is a Linux distribution that provides a free and open-source community-supported computing platform, functionally compatible with its upstream source, Red Hat Enterprise Linux (RHEL). CentOS announced the official joining with Red Hat while staying independent from RHEL, under a new CentOS governing board.


# User Management
## Adding Users
Throughout this tutorial we will be working with the user sammy. Please substitute with the username of your choice.

You can add a new user by typing:
`sudo adduser sammy`

Next, you’ll need to give your user a password so that they can log in. To do so, use the passwd command:
`sudo passwd sammy`

You will be prompted to type in the password twice to confirm it. Now your new user is set up and ready for use! You can now log in as that user, using the password that you set up.

Note: if your SSH server disallows password-based authentication, you will not yet be able to connect with your new username. Details on setting up key-based SSH authentication for the new user can be found in step 4 of Initial Server Setup with CentOS 7.

## Granting Sudo Privileges to a User
If your new user should have the ability to execute commands with root (administrative) privileges, you will need to give the new user access to sudo.

We can do this by adding the user to the wheel group (which gives sudo access to all of its members by default).

To do this, use the usermod command:
`sudo usermod -aG wheel sammy`

Now your new user is able to execute commands with administrative privileges. To do so, simply type sudo ahead of the command that you want to execute as an administrator:
`sudo some_command`

You will be prompted to enter the password of your user account (not the root password). Once the correct password has been submitted, the command you entered will be executed with root privileges.

## Managing Users with Sudo Privileges
To see which users are part of the wheel group (and thus have sudo), you can use the lid function. lid is normally used to show which groups a user belongs to, but with the -g flag, you can reverse it and show which users belong in a group:
`sudo lid -g wheel`
Output
 `sammy(uid=1001)`

The output will show you the usernames and UIDs that are associated with the group. This is a good way of confirming that your previous commands were successful, and that the user has the privileges that they need.

## Deleting Users
If you have a user account that you no longer need, it’s best to delete the old account.

If you want to delete the user without deleting any of their files, type:
`sudo userdel sammy`

If you want to delete the user’s home directory along with the user account itself, type:
`sudo userdel -r sammy`

With either command, the user will automatically be removed from any groups that they were added to, including the wheel group if they were given sudo privileges. If you later add another user with the same name, they will have to be added to the wheel group again to gain sudo access.

# Network Management

View IP address and Netmask:
`ip addr`

View Gateway:
`ip route`

View DNS:
`cat /etc/resolv.conf`

# Disk Management

`free`

`du -h //`

`ll -h`