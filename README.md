# COMPSCI 230 Spring 2021
# Simple Bash Scripts

In this lab we will look at an example of a bash script, and implement a
simple one.

To start working on this lab you must be logged in to the Edlab and in your
`cs230` directory. From this directory run the command:

```
$ git clone https://github.com/umass-cs-230/230-lab-bash-scripts
```

In order to run the script `split.sh`, first do the following:

```
$ chmod +x split.sh
```

Now you can run `split.sh`:

```
$ ./split.sh
```

After running the script, inspect the current directory and the directory and
files it created. What does this script do?

Open `split.sh` in your favorite text editor and examine the code. (Some
questions here about the code that students will answer on Gradescope.)

Look up the usage of `printf` with:

```
man printf
```

Recall that in Project 2, you are asked to read up on the documentation of
`printf` with:

```
man 3 printf
```

What is the difference between these two man pages?

Change **one line** in `split.sh` so that instead of file names

```
0.txt
1.txt
...
10.txt
11.txt
...
100.txt
101.txt
...
```
we have

```
000.txt
001.txt
...
010.txt
011.txt
...
100.txt
101.txt
...
```

Both man pages of `printf` will be helpful here.

Implement a different script called `change_permission.sh`. By running
`change_permission.sh` all files with extension `.txt` in a specified directory
(which you will define in the script) should have read-only permission for all
users.

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
