In Sublime double selection and Ctrl-t to transpose(swap) the two selections.

Swap the current word with the next:
```
dawwP
```


```
" Swap the word the cursor is on with the next word (which can be on a
" newline, and punctuation is "skipped"):
nmap <silent> gw "_yiw:s/\(\%#\w\+\)\(\_W\+\)\(\w\+\)/\3\2\1/<CR><C-o>:noh<CR>
```



# [Vim Cheat Sheet](https://vim.rtorr.com/)

## Cursor movement

- h - move cursor left
- j - move cursor down
- k - move cursor up
- l - move cursor right
- w - jump forwards to the start of a word
- e - jump forwards to the end of a word
- b - jump backwards to the start of a word
- 0 - jump to the start of the line
- 0w - jump to the first non-blank character of the line
- gg - go to the first line of the document
- G - go to the last line of the document
- fx - jump to next occurrence of character x
- tx - jump to before next occurrence of character x
- } - jump to next paragraph (or function/block, when editing code)
- { - jump to previous paragraph (or function/block, when editing code)
- zz - center cursor on screen
- Ctrl + b - move back one full screen
- Ctrl + f - move forward one full screen
- Ctrl + d - move forward 1/2 a screen
- Ctrl + u - move back 1/2 a screen

**Tip** Prefix a cursor movement command with a number to repeat it. For example, 4jmoves down 4 lines.

## Insert mode - inserting/appending text

- i - insert before the cursor
- I - insert at the beginning of the line
- a - insert (append) after the cursor
- A - insert (append) at the end of the line
- o - append (open) a new line below the current line
- O - append (open) a new line above the current line
- ea - insert (append) at the end of the word
- Esc - exit insert mode

## Editing

- r - replace a single character
- J - join line below to the current one
- cc - change (replace) entire line
- cw - change (replace) to the end of the word
- C - change (replace) to the end of the line
- s - delete character and substitute text
- xp - transpose two letters (delete and paste)
- u - undo
- Ctrl + r - redo
- . - repeat last command

## Cut and paste

- yy - yank (copy) a line
- 2yy - yank (copy) 2 lines
- yw - yank (copy) the characters of the word from the cursor position to the start of the next word
- y$ - yank (copy) to end of line
- p - put (paste) the clipboard after cursor
- P - put (paste) before cursor
- dd - delete (cut) a line
- 2dd - delete (cut) 2 lines
- dw - delete (cut) the characters of the word from the cursor position to the start of the next word
- D - delete (cut) to the end of the line
- x - delete (cut) character

## Exiting

- :w - write (save) the file, but don't exit
- :w !sudo tee % - write out the current file using sudo
- :wq or :x or ZZ - write (save) and quit
- :q - quit (fails if there are unsaved changes)
- :q! or ZQ - quit and throw away unsaved changes

## Search and replace

- /pattern - search for pattern
- n - repeat search in same direction
- N - repeat search in opposite direction
