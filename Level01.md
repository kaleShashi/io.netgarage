---
title: level01
url: level1@io.netgarage.org
---
`ssh` to the above url via port no `2224` as mentioned in [io.netgarage.org](http://io.netgarage.org/)

You can use putty client or you can use openSSH with the command `ssh -p 2224 level1@io.netgarage.org`

use __`level1`__ as the password. 

You will get a welcome screen like this.<br>
![](https://user-images.githubusercontent.com/31987272/76157294-c16fb400-612c-11ea-8dac-1350824307bc.PNG)

Running the `ls` command will give you the `README` files.
![](https://user-images.githubusercontent.com/31987272/76157419-a9009900-612e-11ea-9478-8ff6cad5fea2.PNG)

Using the `cat README` command, you can view the level instructions.
![](https://user-images.githubusercontent.com/31987272/76157427-bb7ad280-612e-11ea-95b4-ef911bbc16a0.PNG)

So, in this readme file there are instructions to move to a location called levels which is in the root.

cd to the root
![](https://user-images.githubusercontent.com/31987272/76157434-cdf50c00-612e-11ea-943f-e7828c89ac3a.PNG)


Then cd to the `levels` folder and by running the ls -la command find the executables.
![](https://user-images.githubusercontent.com/31987272/76157442-e107dc00-612e-11ea-815c-c5e51108c690.PNG)

As you can see in the above image, there is a file which has the name `level01` that has an execute permission.

Run this file using `./level01` command and you will be asked for a three digit passcode. Type some random three digit value and it will not work.
6

To find the three digit key, 
Launch the program under gdb:

    $ gdb level01
    
7

Type `info functions` to get information about available functions
8

Then by running the `start` command, gdb will run the programe and provide us with the temporary breakpoint.

9

(If you want you can again run the `info functions` to view runtime functions of the application.)

Run the `set disassembly-flavor intel` and then run `disassemble main` command to get the assembly code of the `main` function of the `level01` programe. And there you need to find the comparison which will be indicated using `cmp`. The value in cmp is a hexadecimal value, we can display its decimal value with `p` or `print` in gdb. Other value `eax` is a register which compare the hexa value with.

Getting the hexa value

10

Exit from gdb using `quit` command and then try our new three digit key as the level01 access key.
11

Type `id` command to verify the `Effective User ID`
12

Finally use the `cat /home/level2/.pass` to get the ssh login password to the next level (level02)
13


So, the key is `XNWFtWKWHhaaXoKI`
