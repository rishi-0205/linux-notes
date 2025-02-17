# SCP(Secure Copy Protocol)

SCP is a command-line utility used to securely transfer files between local and remote hosts, or between two remote hosts, over SSH. It uses SSH for data transfer and provides the same level of security.

## Using SCP with Password Authentication

> scp source_file username@remote_host:/remote/directory

This will copy source_file from the local machine to the /home/user/ directory on the remote machine with IP address 192.168.1.100 . You'll be prompted to enter password for user on the remote machine.

## Using SCP with SSH key Authentication

> scp -i <path-to-.pem-file> source_file username@remote_host:/remote/directory

## Copying a Directory

Using -r flag lets you copy whole directory

## Copying between Two Remote Hosts

> scp username1@remote_host1:/path/to/file username2@remote_host2:/path/to/destination

## Copying files from remote to local

> scp username@remote_host:/path/to/file /path/to/destination/on/local/system
