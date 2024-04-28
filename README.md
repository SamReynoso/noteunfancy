# Note Unfancy
A simple full-featured note management tool.


## Usage

To make the most of Note Unfancy, follow these steps:

1. **Adding Notes**: Use the 'note' command followed by your note text to add 
a new note. For multi-line notes, utilize the `-m` flag.

```shell
→ note This is a new note.
→ note -m
    Notes
    Multi-line Mode:
    Enter '.' on a new line to exit
    > This is a multi-line note.
    > I can exit with a full stop on a new line.
    > .
```
### The Workflow


- **-S to Swap**: Switch between live note files.
- **-a to Archive**: Archive notes for long-term storage.
- **-g to Grep notes**: Use the `-g` flag followed by keyword/s to search.
- **-o to Open notes**: Similar to '-g', this option refine the search further
with dmenu and opens your selection in a text editor.(requires dmenu)

```shell
→ note This is the text with the keyword in it.

→ note -g keyword
~/.note_unfancy/.private/.swap.no
~/.note_unfancy/note.no
2:    This is the note with the keyword in it.

→ note -a
    Archive your Note File? (y/N)
Archival complete

→ note -g keyword
~/.note_unfancy/.private/archive/240425_144735.no:4:    This is the note keywith the word in it.
~/.note_unfancy/.private/.swap.no
~/.note_unfancy/note.no
```

### POSIX Compatibility

Yes, POSIX compliant.

## Installation
-Run this script directly.

### Dependencies
   - ed (optional) This was the default, but I forgot how to use ed.
   - vim or nvim (optional) Redefine the EDITOR variable after the defaults
   section to use something else.
   - bat (optional) Defaults to cat if not present.
   - dmenu (optional?) The '-o' option will not work with out it.
