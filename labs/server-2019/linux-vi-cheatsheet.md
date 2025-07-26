 
 
# Shell Commands
 
|Command|Definition|Command Group|Command Subgroup|
|:-------|:----------------------------------|:-----------|:-----------|
|O|Switch to insert mode and Open line above cursor|vi - insert mode| 
|o|Switch to insert mode and Open line below cursor|vi - insert mode| 
|I|Switch to insert mode and Insert text at beginning of line|vi - insert mode| 
|i|Switch to insert mode and insert text at cursor|vi - insert mode| 
|a|Switch to insert mode and append text after cursor|vi - insert mode| 
|A|Switch to insert mode and Append text at line end|vi - insert mode| 
|Ctrl + C|Interrupt/Kill whatever you are running (SIGINT)|Process control| 
|Ctrl + l|Clear the screen|Process control|
|Ctrl + s|Stop output to the screen (for long running verbose commands). Then use PgUp/PgDn for navigation.|Process control| 
|Ctrl + q|Allow output to the screen (if previously stopped using |command above)|Process control|
|Ctrl + D|Send an EOF marker, unless disabled by an option, this will |close the current shell (EXIT)|Process control| 
|Ctrl + Z|Send the signal SIGTSTP to the current task, which suspends it. To return to it later enter fg 'process name' (foreground)|Process control| 
|&|Sends process to the background| 
|crontab|NEVER RUN WITHOUT AN ARGUMENT, run at LEAST crontab -l to list the schedule
|crontab -l \| grep -i \<searchstring>|Search for specific string in crontab -l
|grep|Search for strings within files|
|grep -i "\<searchstring>" \<filename1> \<filename2> \<filename3>|Syntax to grep (case insensitive) across multiple files|Files|Searching| 
|ls \*\<searchstring\>\*|Searching for a filename containing the string \<searchstring\>|Files|Searching|
|vi|Open file in text editor|||
|cd \<directoryPath\>|Change directory|Files|Navigation|
|ls -lt|List with the latest at the top|Files| 
|su - \<username\>|switch user||| 
|ls|List files|Files|| 
|Ls -l|List files with further info|Files|| 
|Man \<programName\>|View the manual for a program. Use the 'Q' key to exit| 
|Q|Exit manual (while viewing the manual for a program)||| 
|[ALT] + b|Back (left) one word|Cursor|vi| 
|[ALT] + w|Forward (right) one word|Cursor|vi| 
|[ESC] + db|Delete the Word before the cursor|Editing|vi| 
|[ESC] + dw|Delete the Word after the cursor|Editing|vi| 
|TAB|Tab completion for file/directory names. For example, to move to a directory 'sample1'; Type cd sam ; |then press TAB and ENTER. type just enough characters to |uniquely identify the directory you wish to open.|Editing| 
| 
|Special Keys|Text Terminals send characters (bytes), not key strokes.
|Special keys such as Tab, Backspace, Enter and Esc are |encoded as control characters.
|Control characters are not printable, they display in the |terminal as ^ and are intended to have an effect on |applications.
|Special keys
| 
| 
|Ctrl+I|Tab|Special keys||
|Ctrl+J|Newline|Special keys|| 
|Ctrl+M|Enter|Special keys|| 
|Ctrl+[|Escape|Special keys|| 
|Ctrl+2|^@|Special keys|| 
|Ctrl+3|^[ Escape|Special keys|| 
|Ctrl+4|^\\ |Special keys|| 
|Ctrl+5|^]|Special keys|| 
|Ctrl+6|^^|Special keys||
|Ctrl+7|^_ Undo|Special keys|| 
|Ctrl+8|^? Backward-delete-char|Special keys|| 
|Ctrl+v|tells the terminal to not interpret the following character, so Ctrl+v Ctrl-I will display a tab character|Special keys||
|Ctrl+v ENTER|will display the escape sequence for the Enter key: ^M|Special keys||
|!!|Repeat last command|History
| 
| 
|!n
|Repeat from the last command: args n e.g. !:2 for the second |argumant.
|      
|History
| 
| 
|!n:m
|Repeat from the last command: args from n to m. e.g. !:2-3 |for the second and third.
|    
|History
| 
| 
|!n:$
|Repeat from the last command: args n to the last argument.
|      
|History
| 
| 
|!n:p
|Print last command starting with n
|    
|History
| 
| 
|!string
|Print the last command beginning with string.
|      
|History
| 
| 
|!:q
|Quote the last command with proper Bash escaping applied.
|Tip: enter a line of Bash starting with a # comment, then run |!:q on the next line to escape it.
|       
|History
| 
| 
|!$
|Last argument of previous command.
|History
| 
| 
|ALT + .
|Last argument of previous command.
|History
| 
| 
|!*
|All arguments of previous command.
| 
|History
| 
| 
|^abc­^­def
|Run previous command, replacing abc with def
|History
| 
| 
|:n,ns/^/#
| 
| 
|Comment multiple lines
|Where n,n is start line number, end line number
|From <https://dev.to/grepliz/|3-ways-to-comment-out-blocks-of-code-in-vi-6j4>
|
|vi
| 
| 
|:n,n/#/^
|Uncomment multiple lines
|Where n,n is start line number to end line number
|vi
| 
| 
|[ESC]
|Switch to command mode
|Note: most commands execute as typed, except for "colon" |commands which execute when return key is pressed
|vi - command mode
|Cursor
| 
|0
|Go to beginning of line
|vi - command mode
|Cursor
| 
|nG
|Go to line n
|vi - command mode
|Cursor
| 
|$
|Go to end of line
|vi - command mode
|Cursor
|2
|[CTRL] + u
|Scroll up 1/2 screen
|vi - command mode
|Cursor
|2
|[CTRL] + b
|Scroll backward 1 screen
|vi - command mode
|Cursor
| 
|[CTRL] + d
|Scroll down 1/2 screen
|vi - command mode
|Cursor
| 
|[CTRL] + f
|Scroll forward 1 screen
|vi - command mode
|Cursor
| 
|G
|Go to last line
|vi - command mode
|Cursor
| 
|nG
|Go to line n in a file
| 
| 
| 
|:##
|Go to line number ##
|vi - command mode
|Cursor
| 
|(
|Scroll forward by sentence
|vi - command mode
|Cursor
| 
|)
|Scroll back by sentence
|vi - command mode
|Cursor
| 
|w
|Scroll forward by word
|vi - command mode
|Cursor
| 
|E
|Scroll forward by word/go to end of word
| 
| 
| 
|b
|Scroll back by word/go to beginning of word
|vi - command mode
|Cursor
| 
|{
|Scroll forward by paragraph
|vi - command mode
|Cursor
| 
|}
|Scroll back by paragraph
|vi - command mode
|Cursor
| 
|← OR h
|Move left
| 
|Note: n[command key] will move n characters in the direction |of the command
|e.g. 6h will move 6 characters to the left
|vi - command mode
|Cursor
| 
|↓ OR j
|Move down
| 
|Note: n[command key] will move n characters in the direction |of the command
|e.g. 6h will move 6 characters to the left
|vi - command mode
|Cursor
| 
|↑ OR k
|Move up
| 
|Note: n[command key] will move n characters in the direction |of the command
|e.g. 6h will move 6 characters to the left
|vi - command mode
|Cursor
| 
|→ OR l
|Move right
| 
|Note: n[command key] will move n characters in the direction |of the command
|e.g. 6h will move 6 characters to the left
|vi - command mode
|Cursor
| 
|cw
|Change word
|vi - command mode
|Delete text
| 
|dw
|Delete word
|Vi - command mode
|Delete text
| 
|r
|Replace one character
|vi - command mode
|Delete text
| 
|x
|Delete text at cursor
|vi - command mode
|Delete text
| 
|X
|Backspace text at cursor
|vi - command mode
|Delete text
| 
|D
|Delete current to end of line
|vi - command mode
|Delete text
| 
|dd
|Delete entire line (to buffer)
| 
|Note: use ndd to delete n lines to buffer
|vi - command mode
|Delete text
| 
|:n,nd
|Delete lines n-n
|vi - command mode
|Delete text
| 
|yy
|Copy line
|vi - command mode
|Delete text
| 
|nyy
|Copy n lines
|vi - command mode
|editing
| 
|:1,2t3
|Copy lines 1-2 and paste after line 3
|vi - command mode
|editing
| 
|:1,2m3
|Move lines 1-2 and paste after line 3
| 
| 
| 
|P
|Paste above current line
|vi - command mode
|editing
| 
|p
|Paste below current line
|vi - command mode
|editing
| 
|ft
|Find the next t
|vi - command mode
|editing
| 
|J
|Join previous line
|vi - command mode
|editing
| 
|?string
|Search backwards for string
|vi - command mode
|editing
| 
|/string
|Search forwards for string
|vi - command mode
|editing
| 
|n
|Find next string in occurrence
| 
|Question Think this is for parsing through results from ?|string and /string commands
|vi - command mode
|editing
| 
|:%s/oldstring/newstring/cg
|% = entire file
|s = search and replace
|c = confirm
|g = global (all)
|vi - command mode
|editing
| 
|:set ic
|Ignore case during search
|vi - command mode
|editing
| 
|.
|Repeat last command
|vi - command mode
|editing
| 
|u
|Undo previous command
|vi - command mode
|editing
| 
|U
|Undo changes to line
|vi - command mode
|editing
| 
|:w
|Save changes to buffer
|vi - command mode
|Save & quit
| 
|ZZ OR :wq
|Save changes and quit vi
|vi - command mode
|Save & quit
| 
|:w file
|Save file to new file
|vi - command mode
|Save & quit
| 
|:q!
|Quit without saving
|vi - command mode
|Save & quit
| 
|:n,nw file
|Save n to n lines to new file
|vi - command mode
|Save & quit
| 
|:syntax on
|Turn on syntax highlighting
|vi
|settings
| 
|:syntax off
|Turn off syntax highlighting
|vi
|settings
| 
|:set number
|Turn on line numbering
|Note: shorthand command = :set nu
|vi
|settings
| 
|:set nonumber
|Turn off line numbering
|Note: shorthand command = :set nonu
|vi
|settings
| 
|:set ignorecase
|Ignore case when searching
|vi
|settings
| 
|:set noignorecase
|Case sensitive searching (default)
|vi
|settings
| 
|:set autoindent
|Turn on auto-indentation
|vi
|settings
| 
|:set noautoindent
|Turn off auto-indentation
|vi
|settings
| 
|>> 
|Indent
|vi
|settings
| 
|<< 
|Outdent
|vi
|settings
| 
|:set shiftwidth=n
|Set indentation to n spaces
|vi
|settings
| 
|:g/^M/s///g
|Change all Windows CR/LF to UNIX style LF line endings in the |current file
| 
|Note: to enter the ^M command, type
|[CTRL] + V, [CTRL] + M
|vi
|settings
| 
|:
|Enter command line mode (from command mode)
| 
|Note: Enter [ESC] command first if navigating from insert mode
| 
|A colon in the command line indicates that vi is in command |line mode
|vi - command line mode
| 
| 
|quit [ENTER]
|Exit vi when modifications have been saved, or no |modifications have been made
| 
|Note: shorthand command = q [ENTER]
|vi - command line mode
| 
| 
|q! [ENTER]
|Ignore modifications and quit
|vi - command line mode
| 
| 
|w [ENTER]
|Save and return to command mode
|vi - command line mode
| 
| 
|wq [ENTER] OR
|x [ENTER]
|Save and quit
|vi - command line mode
| 
| 
| 
|The Ex mode is similar to the command line mode as it also |allows you to enter Ex commands. Unlike the command-line mode |you won't return to normal mode automatically. You can enter |an Ex command by typing a Q in normal mode and leave it again |with the :visual command. Note that the Ex mode is designed |for Batch processing and as such won't support mappings or |command-line editing.
|vi
| 
| 
|ptree [foldername]
|Eg ptree dss to see processes with PIDs running from within |DSS number - makes it easier to identify what to kill
| 
| 
| 
| 
|psef
|Shows some useful info about runnings jobs or something
| 
| 
| 
|scp
|scp -p qhsz430d:~/bin/frac_load ./frac_load_dev
| 
|Example above copying frac_load script to current working |directory and naming the copied file frac_load_dev
| 
| 
| 
|diff [filename1] [filename2]
|Compare differences line by line in each file
| 
| 
| 
|tail -f [logfile]
|Display end of logfile as it writes on UNIX terminal… very |handy for watching progress of loads logs
| 
| 
| 
|Use one of these lines at end of each statement:
| 
|;
|&&
|||
| 
|Run multiple commands Run multiple commands in one line with |`;`, `&&` and `||` - Linux Tips - DEV Community
| 
| 
| 
|:s/^/# #insert # symbol to comment out lines
|
| 
|
| 
| 
| 
|ESC then k to put the last command in buffer back on your |command line
| 
|!@! = start or end of sqlplus session
 
Anatab = script that analyses the table
Use this to "analyse" the table so that oracle knows how to read the table super fast
Generates an "analyse" on the default analyse parameters
Use in UNIX load scripts after creating any new tables (best practice do it for all new tables)
 
 
Error logging and emailing, identify errors via logs by searching for strings:
"Error:"
For the errors you've manually fed to the
"ORA"
DB generated errors
 
Get a string from terminal to command line super quick - double click the script and then right click on command line, to paste it!!!!!!!!!!
 
Sqlplus initiate session by typing
 
sqlplus /@ENVIRONMENT_USERNAME
 
e.g. for DEV oracle env:
sqlplus /@FINDD1_DSS
 
To execute SQL script, do @scriptname.sql WITHIN THE DIRECTORY WHERE THE SCRIPT IS STORED
 
Terminate SQLplus session by typing exit and entering
 
 
 
 
Shift + A to append to end of line
 
Saving from vi:
Escape -- get out of insert mode
-- enter colon command
:
 
w [filename].[file_extension]
 
:
q
 
Listing files:
 
-- top 10 files
ls -lt | head -10
 
psef - dss created command to just show the processes related to current user
 
[ESC] , K (doesn't need to be at the same time) = put last command from buffer on command line (then use K and J to toggle back and forward through commands)
 
 
[ESC] then / to search prev commands for a string
 
 
 
$ vi <filename> — Open or edit a file.
i — Switch to Insert mode.
Esc — Switch to Command mode.
:w — Save and continue editing.
:wq or ZZ — Save and quit/exit vi.
:q! — Quit vi and do not save changes.
yy — Yank (copy) a line of text.
p — Paste a line of yanked text below the current line.
o — Open a new line under the current line.
O — Open a new line above the current line.
A — Append to the end of the line.
a — Append after the cursor’s current position.
I — Insert text at the beginning of the current line.
b — Go to the beginning of the word.
e — Go to the end of the word.
x — Delete a single character.
dd — Delete an entire line.
Xdd — Delete X number of lines.
Xyy — Yank X number of lines.
g — Go to the last line in a file.
XG — Go to line X in a file.
gg — Go to the first line in a file.
:num — Display the current line’s line number.
h — Move left one character.
j — Move down one line.
k — Move up one line.
l — Move right one character.
 
From <https://www.redhat.com/sysadmin/introduction-vi-editor>

 
Show line numbers in vi = in command mode type :set number
 
image002.png
:w! $BCPDIR/fora/ps4_stg.ps4_raw_lips.ctl
 
Secure copy from DEV to PROD unix boxes (note: -p argument means copy permissions):
scp -p ps4_stg.ps4_raw_lips.ctl qhsz330p:$BCPDIR/fora/
 
-bash-5.0$ su - dss
Password:
qhsz430a:dss(FINDA1)$ cd bin
qhsz430a:dss(FINDA1)$ grep -i hrs_base_employee_v *
qhsz430a:dss(FINDA1)$ grep -i hrs_employee_v *
 
Note: -i argument for grep removes the case sensitivity of the search