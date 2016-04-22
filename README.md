#### pssmashvim

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
set number
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
