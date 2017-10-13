# H(ost)I(nfo)

script dedicated to display infos about your host at the start of a shell session.
it works on linux & osx and requires a terminal with unicode and 256+ colors support.

sample output of `hi -s`
![screenshot](https://github.com/nikopol/hi/blob/master/hi.png?raw=true "hi -s")


## --help
```
hi 0.3

 syntax: hi [-options] [text]

default text is your hostname

options:
  -fg=color         foreground color/gradient
  -bg=color         background color/gradient (not supported yet)
  -c[olor]=1|16|256 set color mode
  -1|16|256         set color mode as well
  -m[ono]           set color mode to 1
  -s[mall]          set small mode
  -font=default     font name (avalaible: default,perl)
  -i[nfo]=kumic     choose info to display

infos can be given as follow:
   k=kernel   u=uptime   c=cpumodel
   m=memory   i=ip

color can be given as follow:
   name          eg: green
   d,d,d         eg: 0,255,0
   h:h:h         eg: 0:ff:0
   hhhhhh        eg: 00ff00
   hhh           eg: 0f0

gradient can be given as follow:
   color-color   eg: white-blue
                     fff-00f

available colors: black,blue,bright_black,bright_blue,bright_cyan,bright_green,bright_magenta,bright_red,bright_white,bright_yellow,cyan,green,grey,magenta,red,white,yellow
 available fonts: default,perl
```

## quick install

```shell
mkdir -p ~/bin
wget -q -O ~/bin/hi https://github.com/nikopol/hi/blob/master/hi?raw=true
chmod +x ~/bin/hi
```

### add it to your shell starting file

bash for example :

```shell
echo '
[ -t 1 ] && [ -f ~/bin/hi ] && ~/bin/hi -s
' >> ~/.bashrc
```
