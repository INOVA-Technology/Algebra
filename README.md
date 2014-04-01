## Algebra

To use:

    ./algebra [-p|-a accuracy] [-v] equation-involving-x

The -p and -a options tell how many digits to round to. The default is 2

-v sets it to verbose mode and it'll tell you a bunch of annoying crap (duh.)

Examples:

    ./algebra -a 3 "(x / 2.0 + 4) * 3 / 100 = 0.225"
    x = 7
    
    ./algebra -v "x - 1 * 2 = 5.2"
    Trying 0 - 1 * 2 = 5.2
    Trying 1 - 1 * 2 = 5.2
    Trying 2 - 1 * 2 = 5.2
    Trying 3 - 1 * 2 = 5.2
    Trying 4 - 1 * 2 = 5.2
    Trying 5 - 1 * 2 = 5.2
    Trying 6 - 1 * 2 = 5.2
    Trying 7 - 1 * 2 = 5.2
    Trying 8 - 1 * 2 = 5.2
    Trying 7.1 - 1 * 2 = 5.2
    Trying 7.2 - 1 * 2 = 5.2
    x = 7.2

    ./algebra -v "(x - 1) * 2 = 5.2"
    Trying (0 - 1) * 2 = 5.2
    Trying (1 - 1) * 2 = 5.2
    Trying (2 - 1) * 2 = 5.2
    Trying (3 - 1) * 2 = 5.2
    Trying (4 - 1) * 2 = 5.2
    Trying (3.1 - 1) * 2 = 5.2
    Trying (3.2 - 1) * 2 = 5.2
    Trying (3.3 - 1) * 2 = 5.2
    Trying (3.4 - 1) * 2 = 5.2
    Trying (3.5 - 1) * 2 = 5.2
    Trying (3.6 - 1) * 2 = 5.2
    x = 3.6

    ./algebra  "x = 1.234" # rounded to 2 places past decimal by default
    x = 1.23

    ./algebra "x - 6 * 2 = sqrt(9)"
    x = 15

Notes/Issues:
* There may be only 1 variable, and that variable must be x
* x must only be on the left side of the equation
* You should use floats when dividing (Ex. x / 2.0 not x / 2)
* 99% of the time, x can't be negative (for now)
