# rsync(Remote Synchronization)

rsync is a powerful tool for syncing files and directories between two locations. It's used to make copy and synchronize files locally and remotely and it has serveral features that make it more efficient and flexible than basic tools like SCP. It's often used for backup, mirroring and incremental file transfers.

#### Key features

1. Efficient file transfer: Only transfers the differences(or "deltas") between the source and the destination, rather than copying the entire file. This makes it much faster for subsequent transfers of the same data.
2. Supports local and remote sync: You can use rsync to transfer files both locally and remotely.
3. Preserves file attributes: rsync can preserve permissions, timestamps, symbolic links, and other file attributes during the file transfer.
4. Uses SSH for secure transfers: rsync can use SSH(like SCP) for encrypted transfers.

## Basic Syntac of rsync

> rsync [options] source destination

Flags:

1. -a: Achive mode (preserves symbolic links, permissions, timestamps, etc)
2. -v: Verbose mode (shows details about the file transfer)
3. -r: Recursively copy directories
4. -z: Compress file data during the transfer(useful for slower connections)
5. -e: Specify the remote shell program(typically used to specify SSH)
6. --delete: Delete files in the destination directory that no longer exist in the source directory
7. --dry-run: Simulate the transfer without actually performing it. Useful for checking what would happen without making changes
8. -P: Combine --partial(keep partially transferred files) and --progress(show progress during transfer)

## Examples

1. Syncing a local directory to another local directory

> rsync -av myfolder/ /home/user/backup/

2. Syncing from local to remote(using ssh)

> rsync -av -e ssh myflder/ username@remote_host:/path/to/transfer

3. Syncing from remote to local

> rsync -av -e ssh username@remote_host:/path/to/file /home/localuser/backup/

4. Delete files in destination that no longer exist in source

> rsync -av --delete myfolder/ /home/user/backup/

5. Running a Dry Run

> rsync -av --dry-run myfolder/ /home/user/backup/

6. Syncing large files over SSH with compression

> rsync -avz -e ssh mylargefile.tar.gz username@remote_host:/path/to/transfer/

7. Remote to remote syntax

> rsync -av -e ssh user1@remote_host1:/path/to/file user2@remote_host2:/path/to/destination
