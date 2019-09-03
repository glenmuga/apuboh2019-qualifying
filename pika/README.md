# Pikachu

For this challenge, we had help from [Team SKR](https://tworeal.appspot.com/).

We are given a .mp4 file that plays a Rick Ashley song.

Using command `file surprisedpikachu.mp4` tell us it's a .mp4 file, so it's in the correct format.

Next we can use command `binwalk surprisedpikachu.mp4` to find any embedded files. It may take a while as the file is quite large. The results shows that there is a MySQL file embedded inside it. 

We can use `binwalk --dd='.' surprisedpikachu.mp4` to extract all files.

Once extracted, the only interesting file is `base32.txt`, it seems someplace where you would hide a flag. We can use command `strings base32.txt | grep apuboh` to search for the flag. However, it does not return any results. The flag must be base32 encoded because of the file name. 

If we try to decode everything in the base32.txt, we get an invalid input because some of the contents are not in base32 format. We do know that the flag is at least 6 characters long because it should contain at least `apuboh`.

We can use `strings -n 7 base32.txt` to only output strings that are at least 7 characters long.

There is only 1 line that is ridiculously long, so we should try that first. 

It is `@MFYHKYTPNAZDAMJZPNXDG5RTOJPWOMDONZQV6ZRQOJTWK5C7ON2WE5BRORWGK435`

Remove the `@` symbol so it would not return any error.

To decode we can use `echo MFYHKYTPNAZDAMJZPNXDG5RTOJPWOMDONZQV6ZRQOJTWK5C7ON2WE5BRORWGK435 | base32 -d` and we will get the flag.

Interestingly enough, this line can be found in the other 2 files that were extracted from `binwalk`.

### Flag

Flag: `apuboh2019{n3v3r_g0nna_f0rget_subt1tles}`
