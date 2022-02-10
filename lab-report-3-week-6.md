# Copy Whole Directories with `scp -r`

First, go to the directory that you want to copy, for example:

```$ cd desktop/markdown-parse```

Then, type 

```$ scp -r . [username]@ieng6.ucsd.edu:~/[directory name]```
Here, `-r` means recursive and `.` is the source

The terminal will start copying the files:![](https://i.imgur.com/OMWgZpV.png)

After logging into your account, you will see the directory being copied:
![](https://i.imgur.com/I90e32O.png)

You can also combine all the commands in one line:
```
scp -r . cs15lwi22ati@ieng6.ucsd.edu:~/markdown-parse; ssh cs15lwi22ati@ieng6.ucsd.edu "cd markdown-parse; javac MarkdownParse.java; java MarkdownParse"
```
![](https://i.imgur.com/wXZJbLt.jpg)
