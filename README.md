# PDF_SHOW_MD5

Some semi-automated scripts which make pdf (version 1.3) shows its own md5.

(This is the first time I have written a project, and it is also the first time I have used python3 outside of the tutorial, kindly for your guidance)



## Requirements:

- python3

- psutil

  ```shell
  pip3 install psutil
  ```

- Linux (Personally, I recommend Debian. Because in Ubuntu unicoll just keep running, but it does not produce any results)



## Install:

 	1. You need to get Unicoll from https://github.com/cr-marcstevens/hashclash and build it.
 	2. Just put exploit folder in the hashclash folder



## USING:

1. There are two argv in exp.py. First argv controls which set of data is running. Second argv controls the beginning in the group of data controlled by the first argv. 

   By default, just using :

   ```shell
   python3 exp.py 0 0
   ```

   and keep adding 1 to the first argv to 31.  All the data will be generated.

2. You may encounter the following fucking situation: a set of data actually ran for an hour and still no results!

   Just delete all related files generated by the argv[1] you are currently stuck. For example: you are trying:

   ```
   python3 exp.py 4 0
   ```

   However, one of this group like 3 stuck for half an hour. Removing file: 4_0.bin, 4_0_c.bin, 4_1.bin, 4_1_c.bin, 4_x.bin and 4_x_c.bin, try previous command again.

3. If you try using 2 many times but still failed. Removing all data created by command:

   ```shell
   python3 exp.py argv[now]-1 0 (like argv[now]==3, argv[now-1]==2)
   ```

   and using command again:

   ```shell
   python3 exp.py argv[now]-1 0
   ```

4. When you have finished all 32 groups data, using:

   ```
   python3 create.py
   ```



## TIPS:

- You may see something uncontrolled in you cloud server:![Image text](https://github.com/GouBa-1/PDF_SHOW_MD5/blob/main/WS(S6J%7B1AP%60_PU4P_4ZDR~1.png)

  Because unicoll may collide some code be mistaken for command, XD

- There are too many uncontrollable results in a Probabilistic Algorithm. So I am not able to write a fully automated script

- File with "_c" is a copy of last result.

- If you want to IDY your own PDF just change files in hex folder


