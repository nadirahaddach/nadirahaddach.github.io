{% include navigation.html %}

# Data Structures Project

### [Python Coding Challenge Files in Github](https://github.com/nadirahaddach/nadirahaddach.github.io/tree/main/python%20files)

### [Runtime](https://replit.com/@nadirahaddach/menupy)

{% include repl.html %}

<iframe frameborder=“0” width=“100%” height=“500px” src=“https://replit.com/@nadirahaddach/nadirahaddachgithubio?lite=true”>

## Code Samples 

### Fibonnaci
```
def fibo(a):
    x = 0
    y = 1
    if a == 1:
        print(x)
    else:
        print(x)
        print(y)
    for i in range(2,a):
        z = x + y
        x = y
        y = z
        print(x+y)
fibo(100)
```

### Loops
```
InfoDb = []
# List with dictionary records placed in a list
InfoDb.append({
    "FirstName": "Katie",
    "LastName": "Hickman",
    "DOB": "December 27",
    "Residence": "San Diego",
    "Favorite_Car_Brands":["Porche", "Ford", "Jeep"]
})

InfoDb.append({
    "FirstName": "Nadira",
    "LastName": "Haddach",
    "DOB": "August 16",
    "Residence": "San Diego",
    "Favorite_Car_Brands","Mercedes","Jeep", "Porche"]
})

# given an index this will print InfoDb content
def print_data(n):
    print(InfoDb[n]["FirstName"], InfoDb[n]["LastName"])  # using comma puts space between values
    print("\t", "Favorite Car Brandss: ", end="")  # \t is a tab indent, end="" make sure no return occurs
    print(", ".join(InfoDb[n]["Favorite_Car_Brands"]))  # join allows printing a string list with separator
    print()
```
    
### Lists
```
def tester1():
    print("For loop")
    for_loop()
    print("While loop")
    while_loop(0)  # requires initial index to start while
    print("Recursive loop")
    recursive_loop(0)  # requires initial index to start recursion


# for loop iterates on length of InfoDb
def for_loop():
    for n in range(len(InfoDb)):
        print_data(n)

# while loop contains an initial n and an index incrementing statement (n += 1)
def while_loop(n):
    while n < len(InfoDb):
        print_data(n)
        n += 1
    return

# recursion simulates loop incrementing on each call (n + 1) until exit condition is met
def recursive_loop(n):
    if n < len(InfoDb):
        print_data(n)
        recursive_loop(n + 1)
    return # exit condition

# Factorial of a number using recursion
def recur_factorial(n):
    if n == 1 or n == 0:
        return 1
    else:
        return n * recur_factorial(n-1)

# this is test driver or code that plays when executed directly, versus import which will not run these statements
def tester2():
    num = int(input("Enter a number for factorial: "))
    # check if the number is negative
    if num < 0:
        print("Sorry, factorial does not exist for negative numbers")
    else:
        print("The factorial of", num, "is", recur_factorial(num))

# Hack 3: Fibonacci.  Write a recursive program to create a fibonacci sequence including error handling for invalid input
```

### Keypad
```
def keypad():
    print()
    numbers = ['1 2 3','4 5 6','7 8 9','  0  ']
    key_pad = '\n'.join(numbers)
    print(key_pad)
```

### Christmas Tree
```
def christmas():
    top = '🎀️'
    top_center = top.center(20, " ")
    print(top_center,end='')
    for i in range(10):
        star = '*' * (2*i)
        center_star = star.center(20, " ")
        print(center_star)
    print('        ||||')
    print('        ||||')
```

### Icecream Animation
```
import time
import os

Color34 = "\u001b[34m"
Color37 = "\u001b[37m"

def icecream1():
    print("         _.-.")
    print("       ,'/ //\ ")
    print("      /// // /)")
    print("     /// // //|")
    print("    /// // ///")
    print("   /// // ///")
    print("  (`: // ///")
    print("   `;`: ///")
    print("   / /:`:/")
    print("  / /  `'") 
    print(" / /")
    print("(_/")
    print("\u001b[34m -------------------------------------------- \u001b[37m")

def icecream2():
    print("              _.-.")
    print("            ,'/ //\ ")
    print("           /// // /)")
    print("          /// // //|")
    print("         /// // ///")
    print("        /// // ///")
    print("       (`: // ///")
    print("        `;`: ///")
    print("        / /:`:/")
    print("       / /  `'") 
    print("      / /")
    print("     (_/")
    print("\u001b[34m -------------------------------------------- \u001b[37m")

def icecream3():
    print("                   _.-.")
    print("                 ,'/ //\ ")
    print("                /// // /)")
    print("               /// // //|")
    print("              /// // ///")
    print("             /// // ///")
    print("            (`: // ///")
    print("             `;`: ///")
    print("             / /:`:/")
    print("            / /  `'") 
    print("           / /")
    print("          (_/")
    print("\u001b[34m -------------------------------------------- \u001b[37m")

def icecream4():
    print("                        _.-.")
    print("                      ,'/ //\ ")
    print("                     /// // /)")
    print("                    /// // //|")
    print("                   /// // ///")
    print("                  /// // ///")
    print("                 (`: // ///")
    print("                  `;`: ///")
    print("                  / /:`:/")
    print("                 / /  `'") 
    print("                / /")
    print("               (_/")
    print("\u001b[34m -------------------------------------------- \u001b[37m")

def icecream5():
    print("                             _.-.")
    print("                           ,'/ //\ ")
    print("                          /// // /)")
    print("                         /// // //|")
    print("                        /// // ///")
    print("                       /// // ///")
    print("                      (`: // ///")
    print("                       `;`: ///")
    print("                       / /:`:/")
    print("                      / /  `'") 
    print("                     / /")
    print("                    (_/")
    print("\u001b[34m -------------------------------------------- \u001b[37m")

def icecream6():
    print("                                  _.-.")
    print("                                ,'/ //\ ")
    print("                               /// // /)")
    print("                              /// // //|")
    print("                             /// // ///")
    print("                            /// // ///")
    print("                           (`: // ///")
    print("                            `;`: ///")
    print("                            / /:`:/")
    print("                           / /  `'") 
    print("                          / /")
    print("                         (_/")
    print("\u001b[34m -------------------------------------------- \u001b[37m")


os.system("clear")
time.sleep(.1)
icecream1()
time.sleep(.5)
os.system("clear")
icecream2()
time.sleep(.5)
os.system("clear")
icecream3()
time.sleep(.5)
os.system("clear")
icecream4()
time.sleep(.5)
os.system("clear")
icecream5()
time.sleep(.5)
os.system("clear")
icecream6()
time.sleep(.5)
os.system("clear")
```

### Ship Animation
```
#funcy.py
import time

# terminal print commands
ANSI_CLEAR_SCREEN = u"\u001B[2J"
ANSI_HOME_CURSOR = u"\u001B[0;0H\u001B[2"
OCEAN_COLOR = u"\u001B[44m\u001B[2D"
SHIP_COLOR = u"\u001B[32m\u001B[2D"
RESET_COLOR = u"\u001B[0m\u001B[2D"

def ocean_print():
    # print ocean
    print(ANSI_CLEAR_SCREEN, ANSI_HOME_CURSOR)
    print("\n\n\n\n")
    print(OCEAN_COLOR + "  " * 35)


# print ship with colors and leading spaces
def ship_print(position):
    print(ANSI_HOME_CURSOR)
    print(RESET_COLOR)
    sp = " " * position
    print(sp + "    |\   ")
    print(sp + "    |/   ")
    print(SHIP_COLOR, end="")
    print(sp + "\__ |__/ ")
    print(sp + " \____/  ")
    print(RESET_COLOR)


# ship function, iterface into this file
def ship():
    # only need to print ocean once
    ocean_print()

    # loop control variables
    start = 0  # start at zero
    distance = 60  # how many times to repeat
    step = 2  # count by 2

    # loop purpose is to animate ship sailing
    for position in range(start, distance, step):
        ship_print(position)  # call to function with parameter
        time.sleep(.1)
```
