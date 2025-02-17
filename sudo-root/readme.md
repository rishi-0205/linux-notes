## sudo vs superuser(root)

In linux, administrative tasks(like installing software, modifiying system files, and managing users) require special previlages. These tasks can be performed using either:

1. Superuser(root) -> The highest-privileged user in linux.
2. sudo(superuser do) -> A command that allows normal users to execute administrative tasks temporarily.

### What is root user?

The root user is the superuser in linux.
Has full control over the system(can modify any file, install/remove software, manage users, etc).
Logging in as root can be dangerous, as a wrong command can break the system.

##### How to switch to root user?

> sudo su

or

> su -

### What is sudo?

sudo allows a normal user to execute commands with root privileges without logging in as root.
Requires authentication(you must enter your own password, not the root password).
Logs every command executed, maming it more secure than directly using root.

##### How to use sudo?

> sudo command

### How to add a user to the sudo group?

Only users in the sudo gorup can use sudo. To ad a user to the sudoers list:

> sudo usermod -aG sudo username

Replace username with actual username

To check if a user has sudo access:

> sudo -l

### Editing sudo Permissions(/etc/sudoers)

To modify sudo access, use:

> sudo visudo

This opens /etc/sudoers for safe editing.
You can grant password-less sudo by adding:

> username ALL=(ALL) NOPASSWD:ALL

### Disabling root Login(for security)

To prevent logging in as root:

> sudo passwd -l root
