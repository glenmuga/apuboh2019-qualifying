# Telegraph-for-the-King

We are given `.txt` file. We use `cat telegraph_for_the_king` to see it's content. This is a snippet of its content.
```
0==0 0=0 00= 000= 0000 00=0 0=0 ==0 0000 0=00 000= =00 00=0 =0= =00 00= =00 00=0 0== 0000 00= 0000 
```

The file is called telegraph, so we shall Google for telegraph decoder to see what we would get. The first result will show morse code but morse code usually in the form of `.` and `-` (dots and dashes). 

What if the all these `0` means a `.` and `=` means a `-`?

Using [cryptii](https://cryptii.com/), we can replace each short with `0` and each long with `=`. Esentially `0` means a `.`(dot) and `=` means a `-`(dash).

We will get an output that doesn't make sense and seems to be a jumbled characters. Here is a snippet of the output: 
```
pruvhfrghlvdfkdudfwhuhqfrglqjvfkhphxvhglqwhohfrppxqlfdwlrqwkdwhqfrghvwhawfkdudfwhuvdvvwdqgduglchgvhtxhqfhvr
```

Using [quipquip](https://quipqiup.com/); a cryptogram solver, we would be able to make sense of the output. What it does is to essentially rearrange the chartacters to make it more legible. 
```
morse code is a character encoding scheme used in telecommunication that encodes text characters as 
standardized sequences of two different signal durations called dots and dashes or dits and dahs morse code 
is named for samuel morse there is no distinction between upper and lower case letters each morse code 
symbol is formed by a sequence of dots and dashes the dot duration is the basic unit of time measurement 
in morse code transmission the duration of a dash is three times the duration of a dot each dot or dash 
within a character is followed by period of signal absence called a space equal to the dot duration your
flag is flag start morse code still in use flag end the letters of a word are separated by a space of 
duration equal to three dots and the words are separated by a space equal to seven dots
```
With the help from my team member, the flag is actually in the sentece `your flag is flag start morse code still in use flag end`.

### Flag
Flag: `apuboh2019{MORSECODESTILLINUSE}`
