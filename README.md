# scripts

## `rsslookup`

Minimalist rss agregator script

## `dirsearch`

Search a patern thru a directory of files

## `prettyman`

Displays manpages in a pretty pdf

## `flasher`

Flashes the terminal (going back and forth between normal and inverse video mode) until the user presses a key

Useful for notifying that a long running command as ended

## `escaper`

Transforms its inputs into a ANSI escapes formated string according to formatting keywords:

 Keyword | Escape Sequence \* | Description
:---:|:---:|:---
`@ESC` | `\e` | The escape character, to produce escape codes that don't have a keyword
`@LF` | `\n` | Go to the next line
`@SPC` | `\s` | A space
`@UL` | `\e[4m` | Underline **On**
`@NOUL` | `\e[24m` | Underline **Off**
`@BD` | `\e[1m` | Bold **On**
`@NOBD` | `\e[22m` | Bold **Off**
`@RESET` | `\e[0m` | Reset Display
`@FG??` | `\e[38;5;..m` | Set Foreground Color to `??` in dark variant (see table below)
`@FGB??` | `\e[38;5;..m` | Set Foreground Color to `??` in bright variant (see table below)
`@BG??` | `\e[48;5;..m` | Set Background Color to `??` in dark variant (see table below)
`@BGB??` | `\e[48;5;..m` | Set Background Color to `??` in bright variant (see table below)

Colors:

Color | Dark ANSI Code | Bright ANSI Code | Name
:---:|:---:|:---:|:---
BK | 0 | 8  | Black
RD | 1 | 9  | Red
GR | 2 | 10 | Green
YL | 3 | 11 | Yellow
BU | 4 | 12 | Blue
VT or PP | 5 | 13 | Purple
AQ | 6 | 14 | Aqua
WH | 7 | 15 | White

\* : `\e` stands for Escape (0x1B), `\n` stands for Line Feed (0x0A), `\s` stands for Space (0x20)

## `xkittyressources`

Updates the kitty terminal configuration if a line containing 
```
#--readxressources--
```
is found in the configuration

The line containing the tag is removed and replace with color settings extracted from the user's `.Xressources` file
