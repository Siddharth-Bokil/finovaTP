# Level 6
> Use find to find the correct file

**Password:** `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`

## Process
Ran `find / -size 33c -user bandit7 -group bandit6` and then `cat /var/lib/dpkg/info/bandit7.password` to find the password.

## What I learnt
`find` has the following flags as well -
  - `-size` can be used to find a file of a specfic size, ie, `33c` meaning 33 bytes
  - `-user` owned by a specific user
  - `-group` owned by a specific group

## References
None


<br><br><br><br>


# Level 7
> Search for a word in a file

**Password:** `dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`

## Process
Ran `grep millionth data.txt` to get the password.

## What I learnt
`grep` prints out the entire line the given word is in.

## References
None


<br><br><br><br>


# Level 8
> Print the line that occurs only once

**Password:** `4CKMh1JI91bUIZZPXDqGanal4xvAg0JM`

## Process
Ran `sort data.txt | uniq -u` to get the password.

## What I learnt
- `sort fileName` orders contents alphabetically
- `uniq -u` prints lines that occur only once.
- `uniq` prints each line once no matter how many times it may have occured.

## References
None


<br><br><br><br>


# Level 9
> Find human-readable text in a file

**Password:** `FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`

## Process
Ran `strings data.txt | grep ==` to find the password.

## What I learnt
`strings fileName` returns all human-readable lines from binary data.

## References
None


<br><br><br><br>


# Level 10
> Decode a base64 file

**Password:** `dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`

## Process
Ran `base64 -d data.txt` to get the flag.

## What I learnt
`base64 -d fileName` decodes a base64 file. Without `-d` it encodes it in base64.
## References
man page of base64
