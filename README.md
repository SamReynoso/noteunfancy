# Note Unfancy
Have you ever wanted a quick way to save a one line note from the terminal, so
you start writing a shell script that will echo to a file, but then it's 300
lines later, and you don't remember the note you wanted to write down anyway?


## Usage

To make the most of Note Unfancy, follow these steps:

1. **Adding Notes**: Use the `note` command followed by your note text to add 
a new note. For multi-line notes, utilize the `-m` flag.

```shell
note This is a new note.
note -m
    Notes
    Multi-line Mode:
    Enter '.' on a new line to exit
    > This is a multi-line note.
    > I can exit with a full stop on a new line.
    > .
```

2. **Retrieving Notes**: Retrieve the last 5 lines of notes or the complete 
file using the `-f` flag.

```shell
note -f
```

3. **Removing Notes**: Remove a note using the `-r` flag.

```shell
note -r
```

## Installation

To install Note Unfancy:

1. Execute the script directly.
2. Ensure a directory named `~/.note_unfancy` exists. Clone the repository 
into this directory and alias the executable as `note`.

### POSIX Compatibility

Note Unfancy is POSIX compliant.

## Advanced Features

In addition to basic note-taking functionality, Note Unfancy offers advanced 
features for enhanced usability. The output from `-h` will show available 
options.

### The Workflow

- **-a to Archive**: Use the `-a` flag to archive notes for long-term storage.
- **-g to Grep notes**: Utilize the `-g` flag followed by a keyword to search 
for notes containing specific terms.

```shell
note This is the note with the keyword in it.

note -g keyword
~/.note_unfancy/.private/.swap.no
~/.note_unfancy/note.no
2:    This is the note with the keyword in it.

note -a
    Archive your Note File? (y/N)
Archival complete

note -g keyword
~/.note_unfancy/.private/archive/240425_144735.no:4:    This is the note keywith the word in it.
~/.note_unfancy/.private/.swap.no
