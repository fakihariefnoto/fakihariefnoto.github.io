## Coloring path in terminal or prompt linux

want to make something cool or boring with your curent terminal view?
here we are some tips to coloring your terminal path
you can do that by opening ``~/.bashrc`` . bashrc is script which run by termeinal when terminal session started
open your terminal and type ``sudo nano ~/.bashrc``
note that root mode have different bashrc
check your root dir by echoing ``echo ~root`` so open your  bashrc ``~root/bashrc``

first uncomment this line
```
#force_color_prompt=yes
```
to
```
force_color_prompt=yes
```

this mean, yeah you want your prompt to be colored
save it and exit.
now run your bashrc again with ``source ~/.bashrc``

or you want to try to make your path style like mind? here we are

```
if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;36m\]\u\[\e[00m\] @ \[\033[01;36m\]\h\[\033[00m\] :#: \[\033[01;33m\]\w\[\033[00m\] >$ '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi
```

i have modified that line after then you can coloring your own with this color cheatsheet and don't forget to end that with \[\033[00m\]

Regular Colors
```
Black=\[\033[0;30m\]        # Black
Red=\[\033[0;31m\]          # Red
Green=\[\033[0;32m\]        # Green
Yellow='\[\033[0;33m\]       # Yellow
Blue=\[\033[0;34m\]         # Blue
Purple=\[\033[0;35m\]       # Purple
Cyan=\[\033[0;36m\]         # Cyan
White=\[\033[0;37m\]        # White
```
Bold
```
BBlack=\[\033[1;30m\]       # Black
BRed=\[\033[1;31m\]         # Red
BGreen=\[\033[1;32m\]       # Green
BYellow=\[\033[1;33m\]      # Yellow
BBlue=\[\033[1;34m\]        # Blue
BPurple=\[\033[1;35m\]      # Purple
BCyan=\[\033[1;36m\]        # Cyan
BWhite=\[\033[1;37m\]       # White
```
Underline
```
UBlack=\[\033[4;30m\]       # Black
URed=\[\033[4;31m\]         # Red
UGreen=\[\033[4;32m\]       # Green
UYellow=\[\033[4;33m\]      # Yellow
UBlue=\[\033[4;34m\]        # Blue
UPurple=\[\033[4;35m\]      # Purple
UCyan=\[\033[4;36m\]        # Cyan
UWhite=\[\033[4;37m\]       # White
```

Background
```
On_Black=\[\033[40m\]       # Black
On_Red=\[\033[41m\]         # Red
```
Reset
```
Color_Off=\[\033[0m'       # Text Reset
```
