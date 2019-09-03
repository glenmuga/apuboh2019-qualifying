# Insult

We are given an `.exe` file. 

We first use command `file insult.exe` to determine the file type. It shows that it is a PE32 executable file. We then use `binwalk insult.exe` to look for any embedded files. It just tells us it is a Microsoft executable file.

Sometimes we can use `strings` command to see if we can get the flag without executing it. 

Use `strings insult.exe | grep apuboh`. It outputs the flag.

### Flag

Flag `apuboh2019{stringz_n_grep_ftw}`
