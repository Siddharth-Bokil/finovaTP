# Learning From Documentation

### Invoke a program by sending it an argument

**Flag:** `pwn.college{QkTiU2Ka1fNqXQ3UnRZv44fQGWB.QX0ITO0wSN2EzNzEzW}`

## Process
Ran `/challenge/challenge --giveflag` as per the documentation and got the flag.


## What I learnt
Documentation can be helpful for understanding arguments


# References
No references used.



<br><br><br><br><br>



# Learning Complex Usage

### Give multiple aarguments to a command

**Flag:** `pwn.college{wTII4nP9SVV12CDeW6Vi8WOyRLa.QX1ITO0wSN2EzNzEzW}`

## Process
Ran `/challenge/challenge --printfile /flag` to obtain the flag.


## What I learnt
Some commands can take multiple arguments.


# References
No references used.




<br><br><br><br><br>



# Reading Manuals

### (title)

**Flag:** `pwn.college{UOfxNFlq7jUjnwXt1jD-8L2CC_6.QX0EDO0wSN2EzNzEzW}`

## Process
Ran `man challenge` to read the manual for challenge. To print the flag, I ran `/challenge/challenge --fzlqjj 718`


## What I learnt
man pages can be useful in understanding arguments and can have hidden information.


# References
No references used.


<br><br><br><br><br>



# Searching Manuals

### Navigate through a man page

**Flag:** `pwn.college{cZldGJ6RZd14wMU2i_OtV4hOCVW.QX1EDO0wSN2EzNzEzW}`

## Process
Ran `man challenge` to read the manual and found that the `--db` argument gives the flag. Ran `/challenge/challenge --db` to get the flag.


## What I learnt
You can search in a man page by typing `/` and then go up/down by typing `n/N`


# References
No references used.


<br><br><br><br><br>


# Searching For Manuals

### Search `man` to find the command to print the flag 

**Flag:** `pwn.college{gYq3p1y4cVaPyt3nrgguUN-Jrir.QX2EDO0wSN2EzNzEzW}`

## Process
This one took longer than usual. I first ran `man man` to read about any arguments that man could take which would be of help. Found `man -k` which searches the descriptions of all commands for a string and returns all matches. One of the matches was `gqpycaytnr (1)       - print the flag!`
The exclamation mark made me think this was it. First thought it was an argument to `/challenge/challenge` then found it the manpage can be opened by running `man gqpycaytnr` which led me to `/challenge/challenge --gqpyca 314` which gave me the flag.


## What I learnt
`man`'s manpage can be accessed by running `man man` and you can search the description of all commands by running `man -k searchString`


# References
No references used.


<br><br><br><br><br>



# Helpful Programs

### Read a manpage using `--help` arugment.

**Flag:** `pwn.college{sQwqo9MKsnKTieB15skwwax3KoF.QX3IDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/challenge --help` and then ran `/challenge/challenge -p` to get the value as 915. Then I ran `/challenge/challenge -g 915` to obtain the flag.


## What I learnt
Some commands have guides that can be read by using the `--help` argument with them.


# References
No references used.


<br><br><br><br><br>



# Help For Builtins

### Find the manpage of a builtin command

**Flag:** `pwn.college{80NwsfHtX_T3k5l_gM_PELMjRrf.QX0ETO0wSN2EzNzEzW}`

## Process
Ran `help challenge`. Then, `challenge --secret 80NwsfHt` gave me the flag.


## What I learnt
To find manpages of builtin commands, use `help commandName`


# References
No references used.
