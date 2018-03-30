# VIM Quick Reference

## Sortcut Keys

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

## Commands

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

## How-Tos

### (1) Copy / Cut and Paste
_Steps:_  
1. In normal mode, move cursor to start position of text to be copied
2. Swtich to visual mode (Short key `v`)
3. Move cursor to last position of text to be copied
4. Press `y` (yank / copy) or `d` (delete / cut)
5. Move cursor to the position to paste the copied (or cut) text
6. Press `p` to paste after the cursor or `P` to paste before the cursor

### (2) Append / Prepend multiple lines with string (e.g. "Hello")
_Steps:_  
1. In normal mode move cursor to the first of the multiple lines
2. Switch to visual block mode (Short key `<Ctrl-v>`)
3. Move cursor to the last of the multiple lines
4. Press `$` (to append) or `^` (to prepend)
5. Press `A` (switch insert mode to append) or `I` (switch insert mode to prepend)
6. Type text to insert (e.g. "Hello" without the quotes)
7. Press `Esc` key

### (3) Search exact string recursively in current directory
_Command:_
```
:vimgrep \<exact\sstring\>/g **/*.ext1 **/*.ext2
```
_Comments:_
- Above command searches recursively in all files with extensions `*.ext1` and `*.ext1`.
- To search in all files just keep `**` instead of `**/*.ext1 **/*.ext2`

### (4) Record and play a macro
_Steps:_
1. In normal mode press `q` followed by any one of the letters `a` to `z` (as register to record macro)
2. Start recording keystrocks to the specified register
3. To stop recording macro, switch to Normal mode and press `q`
4. To play back the recorded macro, press `@` followed by the registered letter (from step 1)
