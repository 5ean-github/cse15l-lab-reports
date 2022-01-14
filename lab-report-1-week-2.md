# Remote Access
In this lab report, I will write about how to log into a course-specific account on `ieng6` for new CSE 15L students.

## Step 1: Installing VScode
You can install VScode [here](https://code.visualstudio.com/). After installing VScode, you should see something like this:

![](https://i.imgur.com/LOlFmST.png)

## Step 2: Remotely Connecting
First, install OpenSSH [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). Then look up your course-specific account for CSE15L [here](https://sdacs.ucsd.edu/~icc/index.php). Next, open terminal in VScode and type the following command:
```
$ ssh [account name]
```
The terminal should say:
```
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

Type `yes` and then type your password. After that, your terminal should be connected to a computer in the CSE basement.

The whole process should look something like this:

![](https://i.imgur.com/AcBeord.png)
![](https://i.imgur.com/PJ5rBIY.png)

## Step 3: Trying Some Commands
Once you are logged into the remote computer, try typing some commands, such as `cd`, `ls`, `pwd`, `mkdir`, and `cp` to see what happens. Here's an example:

![](https://i.imgur.com/n5komLj.png)

## Step 4: Moving Files with `scp`
Now, you'll learn how to copy files from your computer to a remote computer. To do that, go to the directory where the file you want to be copied is, and type the command
```
$ scp [file name] [account name]:[destination]
```
After that, it will ask for your computer's password. After you type your password, you should be able to see the copied file on the remote computer by logging in and using `ls`. Here's an example:

![](https://i.imgur.com/5RVwpV1.jpg)

## Step 5: Setting an SSH Key
As mentioned before, every time we use `scp`, we have to type our own password, which is very time-consuming. Fortunately, we can avoid this by using `ssh` keys. On terminal, go back to your computer and follow these steps:

![](https://i.imgur.com/iJQFnbq.png)

After that, there should be 2 new files on your computer: `id_rsa` and `id_rsa.pub`, both stored in `.ssh` directory. Now, log in to your remote account, type
```
$ mkdir .ssh
```
and then log out. Then type
```
$ scp [path to .ssh]/.ssh/id_rsa.pub [account name]:~/.ssh/authorized_keys
```
You should be able to use `ssh` and `scp` without typing your password after this.

## Step 6: Optimizing Remote Running
There are some tips to optimize the remote process. First, you can  write a command in quotes at the end of an `ssh` command to directly run it on the remote server. You can also use semicolons to seperate multiple commands on the same line. For example, if you want to copy a local java file and run it on the remote computer, you can do something like this:

![](https://i.imgur.com/NrpTa6r.png)

In this case, there are errors in the Java file, but it shows that the file is being compiled.
