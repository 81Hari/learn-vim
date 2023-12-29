# VIM BASICS

## MODES
1. Normal Mode - esc
2. Insert Mode - i | a | o | I | A | O (FROM NORMAL MODE)
3. Visual Mode - v (FROM NORMAL MODE) 
4. Replace Mode - R (FROM NORMAL MODE) 

## Normal Mode Key-Bindings
***Note:** Number can be binded with key bindings (Eg: Pressing 7 and pressing down arrows makes the cursor goes 7 lines down)

***Note:** "." repeat the last command

### Cursor Navigation
1. Moving Left - left arrow |  h
2. Moving down - down arrow | j
3. Moving Up - up arrow | k 
4. Moving Right - right arrow | l

### Advanced Cursor Navigation
1. w --> Moving Right word by word
2. W --> Moving Right word by word (Seperators will not be considered)
3. b --> Moving Left word by word
4. B --> Moving Left word by word  (Seperators will not be considered)
5. e --> to end of the word
6. 0 --> beginning of the line
7. $ --> end of the line
8. % --> end of the parenthis
9. f[_] --> move to next that character
10. t[_] --> move before next that character
11. F[_] --> move to previous that character
12. T[_] --> move to previous after that character
13. gg --> beginning of the file
14. G --> end of the file
15. :line-number | [0-9+]G --> to that linenumber 

### Enter INSERT MODES
1. i --> to enter insert mode before the focus
2. I --> to enter insert mode from the starting of the line
3. a --> to enter insert mode after the focus
4. A --> to enter insert mode from the end of the line
5. o --> to enter insert mode in new line below
6. O --> to enter insert mode in new line above 

### UNDO-REDO 
1. u --> undo
2. control + r --> redo

### COPY
1. p --> paste below the line
2. P --> paste above the line
3. y + $Nav --> Copy Single Character in the desired the direction 
4. yy | Y --> Copy line

### CUT
1. d + $Nav -> Cut Single Character in the entered the direction
2. dd --> Cut the line
3. D --> Cut from the cursor to end
4. c + $Nav --> Cut Single Character in the entered the direction and enters the insert mode (Changing)
5. cc --> Cut the line and enters the insert mode
6. C -->  Cut from the cursor to end and enters insert mode

### Replace
1. r + 'any character' --> replace single character 

### NORMAL MODE VIM COMMANDS
(: --> to exeucte commands)

1. :q --> to quit vim when no changes are made
2. :q! --> to quit vim when changes are made (Changes will be ignored)
4. :w --> write
5. :wq --> write and quit
6. ! --> to execute linux command (Eg: !pwd)
7. :set number --> to view line number
8. :set relativenumber
9. :set mouse=a
10. :set autoindent
11. :set tabstop=4
12. :set shiftwidth=4
13. :colorscheme= (Press Tab to view the list of schemes)

### VIM configuration file
"~/.vimrc"
- For Permenanent Settings
	- Like set colorscheme
---
## VISUAL MODE (v --> To Enter Visual Mode From Normal Mode)

- $Nav --> To Select
- d --> Delete
- y --> Copy | Yank
 
#COMBINATIONS
1. dw | db --> delete word
2. 2dw --> delete 2 words
3. diw --> delete inner word
4. ciw --> change inner word
5. de --> delete till end of the word
6. d$ --> delete till end of the line
7. d0 --> delete till begining
8. ci" --> change inner quotation
9. ci + "{" | "(" --> change inner
---
# INTERMEIDATE

1. << --> indent to left
2. >> --> indent to right
3. == --> auto indent (Works well for Java and C AND Not For Python)
4. =G --> auto indent whole file
## MODES
1. VISUAL LINE MODE - V
2. VISUAL BLOCK MODE - control + V

## SEARCHING
### Forward Search
1. /[_*] --> Searches the entered in the forward
	- n --> searches next occurence 
	- N --> seacrches previous occurence

### Backward Search
1. ?[_*] --> Searches the entered in the Backward
	- n --> searches next occurence 
	- N --> seacrches previous occurence
### Search Token
1. Select and press #
	- # to next token
	- * to previous token
### Mark a place (waypoint)
1. m + [_] --> Marking
 - ' + [_] -- To jump to that marking

### Replace
- Replace full filr -- > %/text_to_be_replaced/replacement/g
- Replace Selected --> s/text_to_be_replaced/replacement/g

### Register
1. :reg
- we can paste the certain register using "name_of_the_register" + p
- we can copy to certain register using  "name_of_the_register" + y
- "+ --> special register which has content of the clipboard

### Macro
- Manual Register
- Start Recording - qa
- Stop Recording - q
- To execute command
