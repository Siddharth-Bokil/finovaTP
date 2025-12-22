# Cat Command

### Use cat to read out a file

**Flag:** `pwn.college{ILp3lwzrhcj4zO2mi0f6jmFVTtP.QXxcTN0wSN2EzNzEzW}`

## Process
Ran `cat flag` to get the flag.

## What I learned
Cat can be used to append two files and give their output at the same time.

## References
No references used.




<br><br><br><br><br>




# Catting Absolute Paths

### (Title)

**Flag:** `pwn.college{EaJNHxyqFeeN8fPAoqe_gX7NT3V.QX5ETO0wSN2EzNzEzW}`

## Process
Ran `cat /flag` to get the flag

## What I learned
Same as above.

## References
No references used.




<br><br><br><br><br>




# More Catting Practice

### Use cat to read out a file

**Flag:** `pwn.college{kB1VDTbm7fAYr4zg_DegF4qAgc0.QXwITO0wSN2EzNzEzW}`

## Process
Ran `cat /lib/apt/solvers/flag` to get the flag.

## What I learned
Same as above.

## References
No references used.




<br><br><br><br><br>




# Grepping for a Needle in a Haystack

### Use grep to search a file

**Flag:** `pwn.college{coHHI-r4GeiQcM9DYwJnvyX9PF6.QX3EDO0wSN2EzNzEzW}`

## Process
Ran `grep pwn.college /challenge/data.txt` to get the flag.

## What I learned
grep finds a particular string from a file. Syntax for grep: `grep SEARCH_STRING /path/to/file`

## References
No references used.




<br><br><br><br><br>




# Comparing Files

### Use diff to find the differences between any 2 files

**Flag:** `pwn.college{gAlKKSFjyCZKrj5mqVbEQ_Gp6OF.01MwMDOxwSN2EzNzEzW}`

## Process
Ran `diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt` and got
```
57a58
> pwn.college{gAlKKSFjyCZKrj5mqVbEQ_Gp6OF.01MwMDOxwSN2EzNzEzW}
```

## What I learned
diff is used to find the difference between 2 text files. Returns ouput in the form
```
lineNoFromF1 a lineNoFromF2
< Difference in F1
---
> Difference in F2
```

## References
No references used.




<br><br><br><br><br>




# Listing Files

### Use ls to display files in a directory.

**Flag:** `pwn.college{YsLOYFU4TjhHK0mYdT1ww6D9ft-.QX4IDO0wSN2EzNzEzW}`

## Process
Ran `ls /challenge/` to get the name of the run file. 
Ran the file using `/challenge/23172-renamed-run-16925` and got the flag.

## What I learned
Learnt that 'ls' shows files in the specified directory.

## References
No references used.




<br><br><br><br><br>




# Touching Files

### Use touch to create files

**Flag:** `pwn.college{M1FEQ0P0TOUrM4mvyV88nzc5Ajq.QXwMDO0wSN2EzNzEzW}`

## Process
Ran the following commands to get the flag - 
```
touch /tmp/pwn
touch /tmp/college
/challenge/run
```

## What I learned
The touch command is used to create files.

## References
No references used.



<br><br><br><br><br>


# Removing Files

### Use the rm command to remove files

**Flag:** `pwn.college{443FGC8KMB_XksHzp49UjrNiem2.QX2kDM1wSN2EzNzEzW}`

## Process
Ran `rm delete_me` and then ran `/challenge/check` to obtain the flag.

## What I learned
rm can be used to remove files by using the cli.
Syntax: `rm fileName`

## References
No references used.



<br><br><br><br><br>


# Moving Files

### Use the mv command to move files

**Flag:** `pwn.college{o_bNeRzcLI7RFTauwWc_iaDbc22.0VOxEzNxwSN2EzNzEzW}`

## Process
Ran `mv /flag /tmp/hack-the-planet` to move the file and then ran `/challenge/check` to obtain the flag.

## What I learned
mv can be used to move/copy files from one to another.
Syntax: `mv pathToFile1 pathToFile2`

## References
No references used.




<br><br><br><br><br>




# Hidden Files

### Use `ls -a` to see hidden files

**Flag:** `pwn.college{I9P8fnmWNiusNoLxHof39QcMkOI.QXwUDO0wSN2EzNzEzW}`


## Process
Ran `ls -a /` to find the file `.flag-15712707419579`. Then I executed `cat .flag-15712707419579` to obtain the flag. Had some difficulty initially as I was trying to run it instead of catting but soon figured it out.

## What I learned
The `-a` flag can be used with `ls` to display hidden files/files that start with a '.'.

## References
No references used.




<br><br><br><br><br>




# An Epic Filesystem Quest

### Use cat to read out a file

**Flag:** `pwn.college{oc0tsenIUv4ICFM9MlqCsLqbn34.QX5IDO0wSN2EzNzEzW}`

## Process
Ran
```
cd /
ls -a
cat MEMO
```
The clue guided me to `/usr/share/X11/locale/ru_RU.UTF-8`
I then ran
```
ls /usr/share/X11/locale/ru_RU.UTF-8
cat /usr/share/X11/locale/ru_RU.UTF-8/ALERT_TRAPPED
```
That guided me to `/usr/share/javascript/mathjax/unpacked/jax/output/CommonHTML/autoload`
Then,
```
cd /usr/share/javascript/mathjax/unpacked/jax/output/CommonHTML/autoload
ls -a
cat INFO
```
Which then told me about a hidden clue in `/opt/linux/linux-5.4/include/config/pid`
Then,
```
ls -a /opt/linux/linux-5.4/include/config/pid
cat /opt/linux/linux-5.4/include/config/pid/.WHISPER
```
Then,
```
cd /opt/linux/linux-5.4/drivers/staging/fieldbus
cat TEASER
```
Which told me about a trapped clue in `/opt/linux/linux-5.4/drivers/gpu/drm/tilcdc`,
```
ls /opt/linux/linux-5.4/drivers/gpu/drm/tilcdc
cd /usr/share/racket/pkgs/option-contract-lib/racket/contract
cat SNIPPET
```
```
ls /usr/local/lib/python3.8/dist-packages/pwnlib/util/crc/__pycache__
cat /usr/local/lib/python3.8/dist-packages/pwnlib/util/crc/__pycache__/SECRET-TRAPPED
cd /usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Arrows
ls
cat DOSSIER
```
which finally led me to the flag.


## What I learned
I learnt that this can be quite tedious, and it is very easy to get overwhelmned by it.

## References
No references used.



<br><br><br><br><br>



# Making Directories

### Use the mkdir command and make directories

**Flag:** `pwn.college{wgIyPh4K7uzbPaZ2XZl0BT0lnbp.QXxMDO0wSN2EzNzEzW}`

## Process
Ran
```
mkdir /tmp/pwn
cd /tmp/pwn
touch college
/challenge/run
```
to get the flag.

## What I learnt
mkdir creates directories/folders.
Syntax: `mkdir folderName`

## References
No references used.



<br><br><br><br><br>





# Finding Files

### Use the find command to find files

**Flag:** `pwn.college{I0ipyFIymV3nMIasPfmoahmuUuC.QXyMDO0wSN2EzNzEzW}`

## Process
Ran
```
find / -name flag
cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat /opt/linux/linux-5.4/sound/soc/intel/flag
```
and then got the flag in that file.

## What I learnt
Syntax: `find searchSpace -name fileName`
find / -name fileName searches the entire file system, not just the root directory.

## References
No references used.



<br><br><br><br><br>



# Linking files

### Use the mkdir command and make directories

**Flag:** `pwn.college{MqNwbCxn-bkgltPXMQDEGi9vag7.QX5ETN1wSN2EzNzEzW}`

## Process
I ran `ln -s /flag ~/not-the-flag` and then retrieved the flag wit `/challenge/catflag`

## What I learnt
Syntax: `ln -s originalFilePath linkFilePath`

## References
No references used.



<br><br><br><br><br>


