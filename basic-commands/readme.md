# Basic Commands

## ls(List directory contents)

> ls [options] [directory]

Flags:

1. -l: Long list format
2. -a: Show hidden files
3. -h: Human-readable file sizes
4. -R: List directory recursively
5. -t: Sort by modification time, newest first

## cd(Change directory)

> cd [directory]

1. ..: goes one directory back
2. ~: takes to the home directory
3. -: takes you to the previous directory you were in

## cp(Copy files and directories)

> cp [options] <source> <destination>

Flags:

1. -r: Copy directories recursively (used when copying folders)
2. -i: Prompt before overwriting files
3. -u: Copy only when the source file is newer than the destination file.

## mkdir(Make Directory)

> mkdir [options] directory_name

Flags:

1. -p: Create parent directories ad needed.
2. -v: Verbose mode

## rm(Remove files or directories)

> rm [options] [file]

Flags:

1. -r: Remove directories and their contents recursively
2. -f: Force removal, without asking for confirmation
3. -i: Ask for confirmation before each removal

## mv(Move or rename files and directories)

> mv [options] <source> <destination>

Flags:

1. -i: Ask for confirmation before overwiting files
2. -u: Move only when the source file is newer than the destination file or when the destinaion is missing

## touch(Create empty files or change file timestamps)

> touch [options] <file>

Flags:

1. -c: Do not create a new file if it doesn't already exist.
2. -t: Set a specific timestamp(requires a date-time arguement)

## cat(Concatenate and display file content)

> cat [options] <file>

Flags:

1. -n: Number all output lines.
2. -b: number non-blank output lines
3. -E: Display $ at the end of each line

## pwd(Print working directory)

> pwd

## echo(Display a line of text)

> echo [options] <string>

Flags:

1. -n: Suppress the trailing newline
2. -e: Enable interpretation of backslash escapes
