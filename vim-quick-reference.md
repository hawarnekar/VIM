# VIM Quick Reference

### Sortcut Keys

Short Key | Mode | Description
:--------:|:----:|:-----------
u | Normal | Undo
\<Ctrl-r> | Normal | Redo
i | Normal | Insert before cursor
I | Normal | Insert before first non-blank at the beginning of line
a | Normal | Insert after cursor
A | Normal | Insert at the end of line
o | Normal | Insert a new line below current line
O | Normal | Insert a new line above current line
C | Normal | Delete from the cursor position to the end of line and start insert
R | Normal | Enter overwrite mode at cursor position
w | Normal | Move one word right
W | Normal | Move one WORD right
b | Normal | Move one word left
B | Normal | Move one WORD left
\* | Normal | Find word under cursor in current window (forward)
\# | Normal | Find word under cursor in current window (backward)
\<Ctrl-]> | Normal | Follow the hyperlink (in Help window)
\<Ctrl-T> | Normal | Go back to prev topic (in Help window)
v | Normal | Switch to visual mode (select text)
\<Ctrl-v> | Normal | Switch to visual block mode
\% | Normal | Jump to matching paranthesis

### Commands

Command | Description
:-------|:-----------
\:copen | Open quickfix buffer
\:cclose | Close quickfix buffer
\:cnext | Display the next error in the quickfix list
\:cprev | Display the prev error in the quickfix list
\:sort | Sort lines alphabetically
\:sort! | Sort lines alphabetically in reverse order
\:sort i | Sort lines alphabetically, ignore case
\:sort u | Sort lines alphabetically, keeping only unique lines
\:set wrap | Enable text wrapping
\:set unwrap | Disable text wrapping
