# COMPSCI 230 Computer Systems Principles
# Simple Bash Scripts

In this lab we will look at an example of a bash script, and implement a
simple one.

To start working on this lab you must be logged in to the Edlab and in your `cs230` directory, or be in a similar environment on your local machine. 

From this directory run the command:

```
$ git clone https://github.com/marcliberatore/230-lab-bash-scripts.git
```

to make a copy of this lab directory, or use [Github Desktop](https://desktop.github.com), or download and decompress a zip file directly from Github to use locally (the green "Code" button has a "Download ZIP" option). 


In order to be able to run the script `split.sh`, first do the following:

```
$ chmod +x split.sh
```

This will give `split.sh` "execute" permission for all users. Now you can run
`split.sh`:

```
$ ./split.sh
```

After running the script, inspect the current directory and the directory and
files the script created. What does this script do?

Open `split.sh` in your favorite text editor and examine the code. Try to
understand what each line does as much as you can.

Look up the usage of `printf` with:

```
man printf
```

Recall that in Project 2, you were asked to read up on the documentation of
`printf` with:

```
man 3 printf
```

What is the difference between these two man pages?

Modify **one line** in `split.sh` so that instead of file names

```
0.txt
1.txt
2.txt
...
10.txt
11.txt
12.txt
...
100.txt
101.txt
102.txt
...
```
we have

```
000.txt
001.txt
002.txt
...
010.txt
011.txt
012.txt
...
100.txt
101.txt
102.txt
...
```

Both man pages of `printf` will be helpful here.

Now let's implement a different script called `change_permission.sh`. By running
`change_permission.sh` all files with extension `.txt` in a specified directory
(which you will define in the script) should have read-only permission for all
users. In addition, the string "\*\*\*READ ONLY\*\*\*" will be appended (use
`>>`) to each `.txt` file as its last line.

Some hints:

1. You will want to write a `for` loop that goes over every file with extension
`.txt`. See [here](http://linuxcommand.org/lc3_wss0130.php) for more hints of
what it might look like.

2. Check the man page of `chmod` to see how to set file permissions.

3. Read about option `-l` in the man page of `ls` to see how to display file
permissions. (This is useful when you test your script.)

Visit the Gradescope assignment associated with this lab to complete the lab.
You will be asked to answer questions associated with `split.sh` and to submit
your `change_permission.sh` file.
