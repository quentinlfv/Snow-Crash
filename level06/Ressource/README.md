By inspecting the directory, we can identify a `.php` file and an executable.

After analyzing the PHP file, particularly the use of `preg_replace()` with the `/e` modifier, we discover that it is possible to execute an argument as PHP code.

To exploit this behavior, we first need to identify the correct syntax, create a file containing the following payload, and then execute `level05`:

```text
[x ${`getflag`}]
```
${...} allows PHP code to be evaluated, even when placed inside double quotes.

The backticks (`) execute the enclosed command and help bypass automatic escaping.

Source:
https://security.stackexchange.com/questions/151142/understanding-preg-replace-filtering-exploitation