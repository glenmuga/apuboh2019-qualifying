# One

For this challenge, we had helped from [Team SKR](https://tworeal.appspot.com/)

We are given a `.pcapng` file. For any `.pcapng` file, we can open it in `Wireshark`.

In `Wireshark`, it shows there are 116 packets and the only interesting protocol is `TCP`. 

Right click -> Follow -> TCP Stream.
The output shows
```
dir
Desktop  Documents  Downloads  Music  Pictures	Public	Templates  Videos
cd Desktop
echo "there were many gap in flag " > gap.txt
iwconfig
mkdir gap
cd gap
echo "tw0" > numberofgap.txt
echo "thr33" >trash.txt
whoami
root
ls -la
total 16
drwxr-xr-x 2 root root 4096 Aug  6 12:16 .
drwxr-xr-x 4 root root 4096 Aug  6 12:15 ..
-rw-r--r-- 1 root root    4 Aug  6 12:15 numberofgap.txt
-rw-r--r-- 1 root root    6 Aug  6 12:16 trash.txt
mkdir number
cd number
echo "a}yp0{udobnxozwhq923401617999#{}[U&A_'%s7d0*3_!~p9`@von^?d<oA>.I2Z}" > pandai.txt
echo "jebaited" > flag.txt
echo "apuboh2019" > tryme.txt
```

Here are some hints to find the flag.
1. `echo "there were many gap in flag " > gap.txt`
2. `echo "tw0" > numberofgap.txt`
3. `echo "thr33" >trash.txt`

This hints that there are some gaps to get the flag, the gap size is 2 characters long and every 3rd character is the flag.

The only interesting one is this line a}yp0{udobnxozwhq923401617999#{}[U&A_'%s7d0*3_!~p9`@von^?d<oA>.I2Z}

At every 3rd character, remove the last 2 characters.

### Flag
Flag: `apuboh2019{U_s0_p@ndAI}`
