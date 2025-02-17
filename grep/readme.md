# grep(Global Regular Expression Print)

The grep command is used to search for patterns within files. It's one of the most powerful and commonly used text-searching tool in Linux. It allows you to search for text using regular expressions.

## Basic Syntax

> grep [options] 'pattern' [file(s)]

1. pattern: The text or regular expression you want to search for.
2. file(s): The file or files in which to search for the pattern.

If no file is specified, grep will search through the standard input(i.e., the text you enter in the terminal)

## Commonly used options in grep

1. -i: ignore case

> grep -i 'hello' file.txt

2. -r or -R: Recursive search

> grep -r 'pattern' /path/to/directory/

3. -l: List filenames

> grep -l 'pattern' \*.txt

4. -n: Show line numbers

> grep -n 'pattern' file.txt

5. -v: Invert match

> grep -v 'pattern' file.txt

6. -w: Match whole words

> grep -w 'word' file.txt

7. -c: Count matches

> grep -c 'pattern' file.txt

8. -H: Show filenames(default when searching multiple files)

> grep -H 'pattern' \*.txt

9. -o: Show only matching parts

> grep -o 'pattern' file.txt

10. --color: Highlight matches

> grep --color=auto 'pattern' file.txt

## Regular Expression in grep

grep also supports regular expressions(regex), which allows you to create more advanced and flexible search patterns.

1. ^: Anchors the pattern to the beginning of a line
2. $: Anchors the pattern to the end of a line
3. .: Matches any single character
4. \*: Matches zero or more occurences of the previous character
5. []: Matches any one of the characters inside the square brackets
6. |: Acts as a logical OR
7. \: Escape character
