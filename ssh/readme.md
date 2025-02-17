# SSH(Secure Shell)

SSH is a protocol used to securely connect to remote systems over a network. It is commonly used for system administration and management of remote servers.

## Connection using SSH with Password Authentication

> ssh username@hostname_or_ip

example:

> ssh user@192.168.1.100

1. username: The user on the remote machine
2. host_or_ip: The ip address or the hostname of the remote machine

This command will prompt you to enter the password for the user "user" on the remote machine. Once you enter the correct password, you will be connected to the remote machine.

## Connection using SSH with key-based Authentication

#### 1. Generate SSH key pair

> ssh-keygen -t rsa -b 2048

This will generate a public and a private key pair in the default directory(~/.ssh/).

1. -t rsa: Specifies the type of key(RSA in this case).
2. -b 2048: Specifies the key length(2048 bits is recommended)

By default, this will create two files:

1. ~/.ssh/id_rsa -> private key
2. ~/.ssh/id_rsa.pub -> public key

#### 2. Copy the Public Key to the Remote Server

> ssh-copy-id username@hostname_or_ip

For example:

> ssh-copy-id user@192.168.1.100

This will copy the public key(~/.ssh/id_rsa.pub) to the remote server's ~/.ssh/authorized_keys file

#### 3. Connect Using SSH Key

Now that your public key is on the remote server, you can connect using your private key without needing to enter a password.

> ssh -i ~/.ssh/is_rsa username@hostname_or_ip
