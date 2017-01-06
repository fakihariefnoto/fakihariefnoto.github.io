## Adding color message in terminal or prompt linux

```
| |_ ___ | | _____  _ __   ___  __| (_) __ _  | | |
| __/ _ \| |/ / _ \| '_ \ / _ \/ _` | |/ _` | | | |
| || (_) |   < (_) | |_) |  __/ (_| | | (_| | |_|_|
 \__\___/|_|\_\___/| .__/ \___|\__,_|_|\__,_| (_|_)
```

adding message by opening ``~/.bashrc`` . bashrc is script which run bytermeinal when terminal session started
open your terminal and type ``sudo nano ~/.bashrc``
note that root mode have different bashrc
check your root dir by echoing ``echo ~root`` so open your  bashrc ``~root/bashrc``

you can adding message when first open terminal or new session with
```
ORG='\033[01;33m'
PUR='\033[01;34m'
NC='\033[0m'

figlet tokopedia !! | toilet -f term
echo ""
echo -e "   herzlich willkommen ${ORG}fakih${NC}, use ${ORG}this code${NC}" | toilet -f term
echo -e "     think before press ${PUR}[enter]${NC}" | toilet -f term
echo ""
```

you can change the color of  variable ORG or PUR or you can make your own variable
don't forget to end color mode with NC variable. look at code above
you can also make your own message like mind with ``figlet``

Regular Colors
```
Black='\033[0;30m'        # Black
Red='\033[0;31m'          # Red
Green='\033[0;32m'        # Green
Yellow='\033[0;33m'       # Yellow
Blue='\033[0;34m'         # Blue
Purple='\033[0;35m'       # Purple
Cyan='\033[0;36m'         # Cyan
White='\033[0;37m'        # White
```
Bold
```
BBlack='\033[1;30m'       # Black
BRed='\033[1;31m'         # Red
BGreen='\033[1;32m'       # Green
BYellow='\033[1;33m'      # Yellow
BBlue='\033[1;34m'        # Blue
BPurple='\033[1;35m'      # Purple
BCyan='\033[1;36m'        # Cyan
BWhite='\033[1;37m'       # White
```
Underline
```
UBlack='\033[4;30m'       # Black
URed='\033[4;31m'         # Red
UGreen='\033[4;32m'       # Green
UYellow='\033[4;33m'      # Yellow
UBlue='\033[4;34m'        # Blue
UPurple='\033[4;35m'      # Purple
UCyan='\033[4;36m'        # Cyan
UWhite='\033[4;37m'       # White
```

Background
```
On_Black='\033[40m'       # Black
On_Red='\033[41m'         # Red
```
Reset
```
Color_Off='\033[0m'       # Text Reset
```
