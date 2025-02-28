# Environment Variables

Environment variables are dynamic values that affect the processes or programs running on a system. They store system-wide or user-specific configuration information, such as paths, settings, and configuration variables.

## Examples:

1. PATH: Specifies a list of directories that the shell searches for executables.
2. HOME: Represents the current user's home directory.
3. USER: The current logged-in user.
4. SHELL: The current shell being used
5. EDITOR: Defines the default text editor to be used by the programs that require editing

## Setting Environment Variables

#### Temporarily for the current session:

> export VAR_NAME=value

#### Permanently for the User:

> echo "export VAR_NAME=value" >> ~/.bashrc
> source ~/.bashrc

#### System-Wide Variables:

> sudo nano /etc/environment

Now add MY_VAR=value to the file

## .env File

A .env file is used primarily in application development to store environment variables. It’s not a Linux-specific feature, but rather a convention used in many web development frameworks (like Node.js, Python’s Django, Ruby on Rails, etc.).

To load environment variables from a .env file manually in the shell:

> export $(cat .env | xargs)

This command reads .env file, and xargs converts each line into an export statement.
This line can be included in to .bashrc to automate the process.
