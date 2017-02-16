# pssmashvim
##part1
###The basics
enable syntax
```
:syntax enable
```
set syntax
```
:set syntax=apache
```

```
cw //change current word
```
exit file using sudo
```
:w !sudo tee %   //  :w !sudo tee filename   =   cat filename | sudo tee filename
```

```
cw //change word
3cw //change 3 word
ctrl R //redo
```
###editing files
```
:set hlsearch
:set incsearch
```
```
i  //thin long tree listing
s //sort on name
r /reverse sort order
gh //hide/unhide dotfile
R //rename
- //up a directory
x //open with application
d //make dict
D //delete dict
```
replace
```
%s/2\.2/2.3/gc    //c: ask confirmation replace 2.2 to 2.3.     a dot means one char, so need to be escaped
```
change path
```
:cd ~/
:e filename         //edit another file
:e .     //see all files in current dir
```
back to fisst screen [see here](http://stackoverflow.com/questions/256204/close-file-without-quitting-vim-application)
```
:bd
```
```
:b name  //switch to buffer
:bp     //previous buffer
v  visual mode,char mode
V  visual mode,line mode
c delete text(not limit to one char) and go to insert mode
```

###config
```
:set list
:set nolist
:set list?   //show current value
:set list&  //reset
```
set value
```
:set softtabstop=2      //sts
:h softtabstop   //help
```
get options
```
:options
```
```
:set filetype
:colorscheme new
```
###files
set current dict as working dir
```
:set autochdir
```



###window and buffer
```
ctrl-w s  //split window horizontally      v: vertical
ctrl w j //bottom window
ctrl w k //up window
ctrl w J //move window itself down
ctrl w K //move window itself up
ctrl w c  //close window
ctrl w w //cycle cursor clockwise ,  W  clockwise
ctrl w t/b  // move to topleft /bottom right
ctrl w p //previous window
ctrl w T //new tab
ctrl w o //close others
```


```
:ls  //list all buffers
:b3  //go to buffer 3
```
```
bn next buffer
bp previous
bf first
bl last
ba allbuffer
bd delete (close file)
```
##part2
###intro
```
zt //near top
zz //middle
zb //near botton
0 //linestart
^ //first char
gm //middle of line
g$ //line end
Fx  //previous x
; //repeat last jump
, //last oposite direction
m //middle of screen
gk //up screen line
- //up to char
```
```
ctrl b/f //screenup/down
ctrl u/d //screen1/2 up/down
ctrl y/e //scroll line
```
```
set ruler
set number  / set nonumber
set laststatus=2
```
create marks, press m first.
```
ma //create mark
`a  //jump to exact line and column
'a  //beginning and line only
d't  //delete from current position to mark t
`0-`9  //location cursor when you last exited vim `0 is most recent
`` ''  //postion of cursor oflast jump
`. '.  //location of last edit
```
get all marks
```
:marks
```
###Editing
```
I: move to the first non-blank character of line
a: move one charater right
A: move to end of line
o: Open a new line below
O: open a new line above
```








###search and replace
search
```
/         //next
?         //previous
# previous word
* next word
g# pre partial match
g* next partial match
```
find line after current match
```
/x/+1  //next line match x
/x/e+3  //three chars next of x
d/x/e<enter>   //delete from cursor to the end of a search
y?def       //copy from cursor to previous def
```
substitute:
[range]/old/new/ciInp         //I->case sensitive p->print matching lines n->show number of matchse
```
:%s/a/b  //all lines
:s/a/b  //currentline
:.,'a s/a/b   //search from cursor to mark a
```

for 
```
:.,'a s/a/b
```
specify a line
```
+5 //5 lines down
-3 // 3 lines up
$ //last 1 of buffer
1 //line 1 in buffer
't //position of mark t
% //all line in buffer
```
sub next 10 lines only
```
s/a/b/g10
```
in visual mode:
```
'<,'>s/a/b
```
print:
```
:g/a/p
:g/a/# //show line number
:g/a/y  //yank
:g/a/d //delete
```
normal mode
```
g/a/normal newtext   /prepend newtext to every match of a
```
magic vs very magic
```
/\(.y\)\{3}
```
is same as
```
/\v(.y){3}     //better
```
by using \v  
ctrl r pate content of register
######advanced config
```
nmap //normal
imap //insert mode
vmap //visual
map
map! //command and insert mode
```
create abbreviation
```
iab ff firefox
ab ff firefox
```
######folding
```
:set foldermethod=indent/syntax/
```

```
zj: move down fold
zo:open
zc:close
za:toggle
zM reduce all
zR open all
```

######documentation
```
:h autocmd
```
ctrlt
ctrl}
