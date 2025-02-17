# find Command

The find command is used to search for files and directories in a directory hierarchy based on various criteria like name, size, type, modification time, etc. It's a powerful tool for locating files, filtering them, and performing actions on them.

## Basic Syntax

> find [path] [expression]

1. path: The directory where the search starts(defaults to the current directory if not specified)
2. expression: Criteria or options for the search(like searching by name, type, size, etc)

## Common Use Cases for find

1. Find files by Name

> find /path/to/search -name "filename"

2. Find files by Type

> find /path/to/search -type <file-type>

Use f for regular files, d for directories and l for symbolic links in place of <file-type>

3. Find files by size

> find /path/to/search -size <condition><size>

For condition use, + for larger than, - for less than, and ignore for exactly stated size.
For size you can use number and unit. Ex: 100M for 100MB, 10k for 10KB, etc.

4. Find files modified in the last n days

> find /path/to/search -mtime <condition><time-in-days>

for condition use - modified in the last n days, + for modified more than n days, no symbol and 0 for <time-in-days> for modified today.

5. Find and Execute Commands on Found Files

> find /path/to/search -name "\*.log" -exec rm {} \;

-exec: executes a command on each file found.
{}: Placeholder for the current file found by find.
\; : Ends the -exec command

6. Find files by permissions

> find /path/to/search -perm <permission-number>

7. Find files by User or Group

> find /path/to/search -user <user>
> find /path/to/search -group <groupname>

8. Find empty files or directories

> find /path/to/search -empty

9. Combine Criteria

> find /path/to/search -name "\*.txt" -and -mtime -7

You can use -and, -or, -not logical operator for combining criteria.
