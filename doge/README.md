# Doge
### Steganography Challenge 

We are given a zip file, we can unzip it with `unzip le_epic_flag_doge.zip`. Once extracted, we are given the infamous doge picture called le_epic_flag_doge.png. 

We usually start by using `strings` command. `strings le_epic_flag_doge.png | grep apuboh`. No results are given.

We then use `binwalk` command to look for any embedded files. `binwalk le_epic_flag_doge.png`. It shows that is an .gzip compressed data. We can extract it by using `binwalk -e le_epic_flag_doge.png`. 

`binwalk` actually extracted a `.tar` and `.tar.gz` file. 

To extract the `.tar` file by using command `tar --extract -f le_epic_flag_doge.png`.

Output is `hmmmm.docx` file. There are actually 2 ways to solve this. 
##### 1st Way

Opening the `.docx` file in Windows will show an empty file but if you `ctrl + a`, it shows that there are some hidden text. We can just change the font colour to black and it will display the flag.

##### 2nd Way

Word document files can actually be extracted to see the files that make up a docx file. Use `unzip hmmmm.docx` to extract it.

We can use command `grep -rl apuboh` to the find where the flag is hidden.

Explanation: -
- `-r`: recursive to look into all directories.
- `-l`: to display the directories that match `apuboh`.

It tells us the flag is hidden in directory `word/document.xml`. Opening it up we can see the flag that is hidden in 2 parts.

### Flag
Flag `apuboh2019{mfw_d0g3_f14g}`
