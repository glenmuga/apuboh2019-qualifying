# Posh

This challenge was solved by my team member. 

We are given file called `posh`. We use command `file posh` to determine the file type. It shows that it is an `ASCII text, with very long lines`. 

We use `cat posh` to look at the file contents and it shows 
```
iEx( "$( SEt-VariAbLE  'oFs' '' ) " +[STriNg]( '87-114A105X116;101;45X72&111t115F116t32&39r97X112}117;98A111
:104:50:48;49&57-123t112-115X104F95&115t99X114X105&112:116&95}97X116:116}97:99F107X101t114;115}95&108t105-10
7A101t125}39'-spliT 'A' -sPlit'F' -SPlIt 'r'-SPlIt '&'-SpLit't' -SpliT ';' -spLIt'-' -sPLIt':' -sPlIt'X'-SPl
it '}' | foReAch-obJECT { ([iNT]$_ -aS [CHar]) })+" $(Set-iTem 'VArIAbLE:oFs' ' ') ")
```
We are given this code and upon inspecting it, we can recognize it as a Windows Powershell script. We tried running it in powershell but we get an error message saying `This script contains malicious content and has been blocked by your antivirus software`. 

Since we can't run this script, let us look at the code to see what is it trying to do. It uses the `Split` command to remove `A, F, r, &, t, ;, -, :, X`.

To do this, I am going to do it the lazy way and copy this string `87-114A105X116;101;45X72&111t115F116t32&39r97X112}117;98A111:104:50:48;49&57-123t112-115X104F95&115t99X114X105&112:116&95}97X116:116}97:99F107X101t114;115}95&108t105-107A101t125` into Microsoft word.

Just use the replace function to replace the characters with a space. 

The output is `87 114 105 116 101 45 72 111 115 116 32 39 97 112 117 98 111 104 50 48 49 57 123 112 115 104 95 115 99 114 105 112 116 95 97 116 116 97 99 107 101 114 115 95 108 105 107 101 125 39`

We need an integer decoder to get the flag. I used [this](https://cryptii.com/).
This will return the flag.

### Flag
Flag: `apuboh2019{psh_script_attackers_like}`
