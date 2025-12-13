# Level 0

### Find password in readme

**Password:** `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`

## Process
Ran `ssh bandit0@bandit.labs.overthewire.org -p 2220` to connect. Ran `cat readme` and found the password. Ran `exit`.

## What I learnt
Exit to connect to next level

## References used
None


<br><br><br><br>


# Level 1

### Read a file

**Password:** `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`

## Process
Ran `cat /home/bandit1/-` to get the password since `cat -` did not work.

## What I learnt
-

## References used
None


<br><br><br><br>


# Level 2

### Read a file with spaces in its name

**Password:** `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

## Process
Ran `cat /home/bandit2/--spaces\ in\ this\ filename--` to read the password.

## What I learnt
Prepend `\` before spaces to call a file having spaces.

## References used
None


<br><br><br><br>


# Level 3

### Read a hidden file

**Password:** `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`

## Process
Ran `cd inhere` and then `ls -al`. Then running `cat ./...Hiding-From-You` gave me the flag.

## What I learnt
-

## References
None


<br><br><br><br>


# Level 4

### Find the human readable file

**Password:** `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`

## Process
Ran `cd inhere/` and then `ls- al` to find 10 files in the directory. Catted all the files to find the `-file07` holding the flag.

## What I learnt
Files starting with `-` can be called by `./` before them.

## References
None


# Level 5

### Use find to find the correct file

**Password:** `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`

## Process
Ran `cd inhere/` and `ls -al` to see a bunch of directory having a bunch of files. Ran `find . -size 1033c ! -executable` to get the flag.

## What I learnt
Find can search for a specfic file size and executability. `c` stands for characters.

## Refereneces
Used [this](https://unix.stackexchange.com/questions/313442/find-human-readable-files)
