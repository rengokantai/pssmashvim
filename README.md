#### pssmashvim
#####part1
######The basics
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
######editing files
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

######config
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
######files
set current dict as working dir
```
:set autochdir
```
######window and buffers
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
//stop at 4:30

#####part2
######intro
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
