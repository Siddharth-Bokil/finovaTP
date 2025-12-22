
# The Root

### Invoke a program using its absolute path

**Flag:** `pwn.college{QpQGRsRE67yqk2qdTSZ3US0LnHL.QX4cTO0wSN2EzNzEzW}`

## Process
Accessed the program by its absolute path, ie, ```/pwn```

## What I learned
Linux file system, absolute and relative paths, meaning of various notations, usage of different files such as usr, bin, proc, etc.
'.' - Current directory
'..' - Previous directory
'/' - Run/Invoke

## References
No references used.




<br><br><br><br><br>




# Program and Absolute Paths

### Run a program by reffering to its absolute path

**Flag:** `pwn.college{8XOhp88JQhmGBNW1CKNdS-uopri.QX1QTN0wSN2EzNzEzW}`

## Process
Ran the program by reffering to its absolute path, ```/challenge/run```

## What I learned
Linux file system, absolute and relative paths, meaning of various notations, usage of different files such as usr, bin, proc, etc.
'.' - Current directory
'..' - Previous directory
'/' - Run/Invoke

## References
No references used.




<br><br><br><br><br>




# Position Thy Self

### Invoke the program using its absolute path from a particular directory

**Flag:** `pwn.college{I3gm6jqBXCP9V3z3bVEujjLAm9r.QX2QTN0wSN2EzNzEzW}`

## Process
Ran the program to get the path and then went to `/var/lib/apt/lists directory` using the `cd` command and then ran the file using its absolute path, `/challenge/run`

## What I learned
Learnt using the cd command, and meaning on ~ 

## References
No references used.



<br><br><br><br><br>



# Position elsewhere

### Invoke the program using its absolute path from a particular directory

**Flag:** `pwn.college{sSvpSZy9SPCmer-paHclfyUVymI.QX3QTN0wSN2EzNzEzW}`

## Process
Ran the program to get the path and then went to `/usr/share/zoneinfo/posix/Asia` using the `cd` command and then ran the file using its absolute path, `/challenge/run`

## What I learned
Same as the last challenge, nothing different.

## References
No references used.



<br><br><br><br><br>



# Position yet elsewhere

### Invoke the program using its absolute path from a particular directory

**Flag:** `pwn.college{Aipep88L8aMnFlX5E6OQAW_lz2O.QX4QTN0wSN2EzNzEzW}`

## Process
Ran the program to get the path and then went to `/sys` using the `cd` command and then ran the file using its absolute path, `/challenge/run`

## What I learned
Same as the last challenge, nothing different.

## References
No references used.



<br><br><br><br><br>



# Implicit relative paths, from /

### Ran a program by using its relative path.

**Flag:** `pwn.college{sskK1_el0Dr0m2CVVtDe9H20tyG.QX5QTN0wSN2EzNzEzW}`

## Process
Went to the `/` using the `cd` command and then ran the file using a relative path, `challenge/path`

## What I learned
Relative paths. In this specific case it wouldn't have mattered as I was already at the root directory so absolute path = relative path.

## References
No references used.




<br><br><br><br><br>




# Explicit relative paths, from /

### Ran a program by using its relative path but with '.'(cwd)

**Flag:** `pwn.college{g2_FdFgKhxhQSRdDT8fHLgWgcCs.QXwUTN0wSN2EzNzEzW}`

## Process
Went to the `/` directory using the `cd` command and then ran `./challenge/run/` to get the flag

## What I learned
Relative paths, '.' - Current working directory.

## References
No references used.



<br><br><br><br><br>



# Implicit relative path

### Running a program while being in the same directory as the program

**Flag:** `pwn.college{wCZG8TPCvDToaQ9-pRDT6dmcgEd.QXxUTN0wSN2EzNzEzW}`

## Process
Went to the `/challenge` directory using cd and then ran `./run` to get the flag.

## What I learned
Use case of `./` is so that if files that have the same name in the `/`(root) directory are not confused with other local ones. `./` acts a run command.

## References
No references used.



<br><br><br><br><br>



# Home Sweet Home

### 

**Flag:** `pwn.college{AMySS6G0Fsh5YsqBLk0Qb-Fa9wA.QXzMDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run ~/a` where 'a' is the name of the file where I'm copying the flag.
Initially I thought I would have to cat the file but there was no need to do so.


## What I learned
'~' is shorthand for /home/hacker/

## References
No references used.

<br><br><br><br><br>




