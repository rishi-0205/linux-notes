# which - Locate Executable Paths of Commands

The which command helps find the full path of a command or executable in your system. It searches the directories listed in the $PATH environment variable and tells you where the executable is located.

## Basic Syntax

> which command_name

This will return the command's executable location. If nothing is returned, the command doesn't exist.

> which -a python

This lists all the locations of python, in order of priority.
