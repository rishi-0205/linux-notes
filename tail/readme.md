# Tail

tail display the last 10 lines of a file by default

## Basic Syntax

> tail [options] filename

#### Examples

1. Display the last 10 lines:

> tail file.txt

2. Display the last <n> lines:

> tail -n <n> file.txt

3. Display the last <n> bytes:

> tail -c <n> file.txt

4. Monitor a file in real-time(useful for logs):

> tail -f /var/log/syslog

-f keeps showing new lines as the file updates
