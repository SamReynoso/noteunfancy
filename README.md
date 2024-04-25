# Note Unfancy
Have you ever wanted a quick way to save a one line note from the terminal, so
you start writing shell script that will echo to a file, but then it's 300
lines later, and you don't remember the note you wanted to write down anyway?

If the answer is NO then you're in luck. Note Unfancy is here.

## Usage
Add by passing the note as arguments, or use the -m flag to enter multi-line
mode.

```shell
note This is a new note.
note -m

    Notes
Multi-line Mode:
Enter '.' on a new line to exit
>    This is a multi-line note.
>    I can exit with a full stop on a new line.
>    .
```

Pass zero args to read the last 5 line, or use the -f flag for the complete
file.

```shell
note -f
Thu Apr 25 11:47:35 AM PDT 2024
    This is a new note.
--------
|    This is a multi-line note.
|    I can exit with a full stop on a new line.
--------
```

Remove a note with the r flag.

```shell
note -r
--------
|    This is a multi-line note.
|    I can exit with a full stop on a new line.
--------
Do you want to remove this note? (y/N)
```

# Installation
Run this script directly.

This script will look for a directory at ~/.note_unfancy. You could simply
create that directory, and put the script there, or clone the repo inside, and
alias the executable to note.

### POSIX
This script was written in Bash.

# Advanced Features
The output from -h will show available options.

### The workflow
- -a to Archive
- -q to Grep notes

```shell
note This I the note with the word in it.

note -g word
~/.note_unfancy/.private/.swap.no
~/.note_unfancy/note.no
2:    This I the note with the word in it.

note -a
    Archive you Note File? (y/N)
Archival complete

note -g word
~/.note_unfancy/.private/archive/240425_144735.no:4:    This I the note with the word in it.
~/.note_unfancy/.private/.swap.no
~/.note_unfancy/note.no
```
