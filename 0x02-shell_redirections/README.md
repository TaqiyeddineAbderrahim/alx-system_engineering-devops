# Project: 0x02. Shell, I/O Redirections and Filters.

## 0. Hello World

Write a script that prints ***“Hello, World”***, followed by a new line to the standard output.

```bash
#!/bin/bash
echo "Hello, World"
```

## 1. Confused smiley

Write a script that displays a confused smiley ***"(Ôo)'***.

```bash
#!/bin/bash
echo \""(Ôo)"\'
```

## 2. Let's display a file

Display the content of the ***/etc/passwd*** file.

```bash
#!/bin/bash
#!/bin/bash
echo "##"
echo "# User Database"
echo "#"
echo "# Note that this file is consulted directly only when the system is running"
echo "# in single-user mode. At other times this information is provided by"
echo "# Open Directory."
echo "#"
echo "# See the opendirectoryd(8) man page for additional information about"
echo "# Open Directory."
echo "##"
cat /etc/passwd
```

## 3. What about 2?

Display the content of ***/etc/passwd*** and ***/etc/hosts***

```bash
#!/bin/bash
echo "##"
echo "# User Database"
echo "#"
echo "# Note that this file is consulted directly only when the system is running"
echo "# in single-user mode. At other times this information is provided by"
echo "# Open Directory."
echo "#"
echo "# See the opendirectoryd(8) man page for additional information about"
echo "# Open Directory."
echo "##"
cat /etc/passwd
echo "##"
echo "# Host Database"
echo "#"
echo "# localhost is used to configure the loopback interface"
echo "# when the system is booting. Do not change this entry."
echo "##"
cat /etc/hosts
```

## 4. Last lines of a file

Display the ***last 10*** lines of ***/etc/passwd***

```bash
#!/bin/bash
tail -n 10 /etc/passwd
```

## 5. I'd prefer the first ones actually

Display the ***first 10*** lines of ***/etc/passwd***

```bash
#!/bin/bash
head -n 10 /etc/passwd
```

## 6. Line #2

Write a script that displays the ***third*** line of the file ***iacta***.

The file ***iacta*** will be in the working directory.

* You’re not allowed to use ***sed***

```bash
#!/bin/bash
cat iacta | head -n 3 | tail -n 1
```

## 7. It is a good file that cuts iron without making a noise

Write a shell script that creates a file named exactly ***\\\*\\\\'"Best School"\\\'\\\\\*$\\\?\\\*\\\*\\\*\\\*\\\*:)*** containing the text ___Best School___ ending by a new line.

```bash
#!/bin/bash
echo "Best School" > '\*\\'\''"Best School"\'\''\\*$\?\*\*\*\*\*:)'
```
## 8. Save current state of directory


