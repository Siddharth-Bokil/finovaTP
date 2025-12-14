# Level 0
> Find password in readme

**Password:** 
## Process
I connected to the server using `ssh bandit0@bandit.labs.overthewire.org -p 2220`. Once logged in, I listed the files in the home directory and noticed a file named `readme`. I used `cat readme` to display its contents, which contained the password for the next level. After noting it down, I exited the session using `exit`.

## Password
```ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If```


## What I learnt
Exit to connect to next level

## References used
None


<br><br><br><br>


# Level 1
> Read a file

## Process
After logging in as `bandit1`, I checked the home directory and found a file named `-`. Since filenames starting with `-` can be interpreted as command options, I provided the full path to the file. Running `cat /home/bandit1/-` correctly displayed the contents of the file, revealing the password.

## Password
```263JGJPfgU6LtdEvgfWU1XP5yac29mFx```

## What I learnt
Files are read through the cat command.

## References used
None


<br><br><br><br>


# Level 2
> Read a file with spaces in its name

## Process
Once logged in, I listed the files and found one with spaces in its name. Since spaces break command arguments, I escaped each space using a backslash. Running `cat /home/bandit2/--spaces\ in\ this\ filename--` allowed me to correctly reference the file and read the password.

## Password
```MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx```

## What I learnt
Prepend `\` before spaces to call a file having spaces.

## References used
None


<br><br><br><br>


# Level 3
> Read a hidden file

## Process
After logging in, I navigated into the `inhere` directory using `cd inhere`. A normal `ls` command didn’t show any useful files, so I used `ls -al` to list all files, including hidden ones. This revealed a hidden file named `...Hiding-From-You`. Running `cat ./...Hiding-From-You` displayed the password.

## Password
```2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ```

## What I learnt
Hidden files are accessed throught `ls -a`.

## References
None


<br><br><br><br>


# Level 4
> Find the human readable file

## Process
I moved into the `inhere/` directory and listed all files using `ls -al`. This showed multiple files with similar names, all starting with `-file`. Since files starting with `-` can cause issues, I accessed them using `./`. I checked each file using `cat ./-fileXX` until I found the one that produced readable text. The human-readable file turned out to be `-file07`, which contained the password.

## Password
```4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw```

## What I learnt
Files starting with `-` can be called by `./` before them.

## References
None


# Level 5
> Use find to find the correct file

## Process
First, I navigated into the `inhere/` directory using `cd inhere/`. Inside, there were many subdirectories, each containing multiple files, so manually checking files was not practical. Based on the level hint, I knew the target file had a specific size and was not executable. To narrow it down efficiently, I used the `find` command with filters as `find . -size 1033c ! -executable`. This searched through all subdirectories for files exactly 1033 bytes in size and excluded any executable files. The command returned a single matching file. I then used `cat` on that file to read the password.

## Password
```HWasnPhtq9AVKe0dmk45nxy20cvUa6EG```

## What I learnt
Find can search for a specfic file size and executability. `c` stands for characters.

## Refereneces
Used [this](https://unix.stackexchange.com/questions/313442/find-human-readable-files)
