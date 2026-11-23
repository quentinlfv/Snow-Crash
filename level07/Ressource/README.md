We discover an executable named `level07` in the current directory.

```text
level07@SnowCrash:~$ ls -l level07
-rwsr-sr-x 1 flag07 level07 8805 Mar  5  2016 level07
```
The executable has the SUID bit set and is owned by `flag07`. This means it runs with the privileges of the flag07 user, potentially allowing us to retrieve the flag directly.

To better understand its behavior, we use the `strings` command:
```text
level07@SnowCrash:~$ strings ./level07
LOGNAME
/bin/echo %s
```
We notice that the program references the `LOGNAME` environment variable. After running a few tests, we can confirm that its value is passed to the `echo` command.

After researching `shell injection` vulnerabilities, we learn that the `semicolon (;)` can be used to separate commands, allowing another command to be executed.

We can therefore modify the `LOGNAME` environment variable to inject our own command:
```text
level07@SnowCrash:~$ export LOGNAME=";getflag"
```
This allows us to execute getflag with the privileges of the flag07 user.