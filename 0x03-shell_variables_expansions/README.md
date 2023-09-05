# Project: 0x03. Shell, init files, variables and expansions.

## 0. <o>

Create a script that creates an alias.

* Name: ***ls***
* Value: ___rm *___

```bash
#!/bin/bash
alias ls="rm *"
```

## 1. Hello you

Create a script that prints ___hello user___, where ___user___ is the current Linux user.

```bash
#!/bin/bash
echo hello $USER
```

## 2. The path to success is to take massive, determined action

Add ___/action___ to the ___PATH___. ___/action___ should be the last directory the shell looks into when looking for a program.

```bash
#!/bin/bash
export PATH=$PATH:/action
```

## 3. If the path be beautiful, let us not ask where it leads

Create a script that ___counts___ the number of directories in the ***PATH***.

```bash
#!/bin/bash
echo $PATH | tr ":" "\n" | wc -l
```

## 4. Global variables

Create a script that lists environment variables.

```bash
#!/bin/bash
printenv
```

## 5. Local variables

```bash
#!/bin/bash
set
```

## 6. Local variable

Create a script that creates a new local variable.

* Name: ___BEST___
* Value: ___School___

```bash
#!/bin/bash
BEST="School"
```

## 7. Global variable

Create a script that creates a new global variable.

* Name: ___BEST___
* Value: ___School___

```bash
#!/bin/bash
export BEST="School"
```

## 8. Every addition to true knowledge is an addition to human power

Write a script that prints the result of the addition of 128 with the value stored in the environment variable ___TRUEKNOWLEDGE___, followed by a new line.

```bash
#!/bin/bash
echo $(( 128 + $TRUEKNOWLEDGE ))
```

## 9. Divide and rule

Write a script that prints the result of ___POWER___ divided by ___DIVIDE___, followed by a new line.

* ___POWER___ and ___DIVIDE___ are environment variables

```bash
#!/bin/bash
echo $(( $POWER / $DIVIDE ))
```

## 10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath

Write a script that displays the result of ___BREATH___ to the power ___LOVE___

* ___BREATH___ and ___LOVE___ are environment variables
* The script should display the result, followed by a new line

```bash
#!/bin/bash
echo $(( BREATH**LOVE ))
```

## 11. There are 10 types of people in the world -- Those who understand binary, and those who don't

Write a script that converts a number from base 2 to base 10.

* The number in base 2 is stored in the environment variable ___BINARY___
* The script should display the number in base 10, followed by a new line

```bash
#!/bin/bash
echo $((2#$BINARY))
```

## 12. Combination

Create a script that prints all possible combinations of two letters, except oo.

* Letters are lower cases, ___from a to z___
* One combination per line
* The output should be alpha ordered, starting with ___aa___
* Do not print ___oo___
* Your script file should contain ___maximum 64 characters___

```bash
#!/bin/bash
echo {a..z}{a..z} | tr ' ' '\n' | grep -v "oo"
```

## 13. Floats

Write a script that prints a number with two decimal places, followed by a new line.

The number will be stored in the environment variable ___NUM___.

```bash
#!/bin/bash
printf "%.2f\n" $NUM
```

## 14. Decimal to Hexadecimal

Write a script that converts a number from base 10 to base 16.

* The number in base 10 is stored in the environment variable ___DECIMAL___
* The script should display the number in base 16, followed by a new line

```bash
#!/bin/bash
printf '%x\n' $DECIMAL
```

## 15. Everyone is a proponent of strong encryption

Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.

```bash
#!/bin/bash
tr 'A-MN-Za-mn-z' 'N-ZA-Mn-za-m'
```

## 16. The eggs of the brood need to be an odd number

Write a script that prints every other line from the input, starting with the first line.

```bash
#!/bin/bash
paste - - | cut -f1
```

## 17. I'm an instant star. Just add water and stir.

Write a shell script that adds the two numbers stored in the environment variables ___WATER___ and ___STIR___ and prints the result.

* ___WATER___ is in base ___water___
* ___STIR___ is in base ___stir___.
* The result should be in base ___bestchol___

```bash
#!/bin/bash
printf '%o\n' $(( 5#$( echo $WATER | tr water 01234) + 5#$( echo $STIR | tr stir. 01234 ) )) | tr 01234567 bestchol
```
