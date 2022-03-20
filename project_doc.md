{% include navigation.html %}

# Data Structures Project

### [Python Coding Challenge Files in Github](https://github.com/nadirahaddach/nadirahaddach.github.io/tree/main/python%20files)

### [Runtime](https://replit.com/@nadirahaddach/menupy)

<iframe frameborder=“0” width=“100%” height=“500px” src=“https://replit.com/@nadirahaddach/nadirahaddachgithubio?lite=true”></iframe>

## Code Samples 

### Swap
```
def swap(age1, age2):
    temp = age1
    age1 = age2
    age2 = temp
    print("After Swap",(age1, age2))
number1 = int(input(" Please Enter the First number : "))
number2 = int(input(" Please Enter the Second number : "))
print("Before Swap",(number1, number2))
swap(number1, number2)
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
