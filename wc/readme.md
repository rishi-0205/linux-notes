# WC(Word Count)

The wc(word count) command is used to count lines, words, characters, and bytes in a file or input.

## Basic Syntax

> wc [options] [file]

If no file is provided, wc reads input from stdin.

## Commonly Used Options in wc

1. -l: Count the number of lines
2. -w: Count the number of words
3. -c: Count the number of bytes
4. -m: Count the number of characters(differs from -c for multibyte charaters)
5. -L: Print the length of the longest line in the file

## Using wc with other commands

1. Count the number of files in a directory

> ls | wc -l

2. Count the number of words in a specific pattern

> grep "error" logfile.txt | wc -w

3. Count the number of running processes

> ps aux | wc -l
