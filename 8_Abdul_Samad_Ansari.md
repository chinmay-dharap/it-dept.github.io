# Problem Statement 1: Strings in the box

## Submitted Code:

```
list = input()
print("****************")
print("*", list[2], "           *")

print("*", list[7:19], "*")

print("*", list[23:25], "          *")

print("*", list[29:34], "       *")

print("*", list[38:47], "   *")

print("****************")

```

# Problem Statement 2: English to Morse

## Submitted Code:

```
string = input()
morse = []
for index in string:
    if index.lower() == "a":
        morse.append(".-")
    elif index.lower() == "b":
        morse.append("-...")
    elif index.lower() == "c":
        morse.append("-.-.")
    elif index.lower() == "d":
        morse.append("-..")
    elif index.lower() == "e":
        morse.append(".")
    elif index.lower() == "f":
        morse.append("..-.")
    elif index.lower() == "g":
        morse.append("--.")
    elif index.lower() == "h":
        morse.append("....")
    elif index.lower() == "i":
        morse.append("..")
    elif index.lower() == "j":
        morse.append(".---")
    elif index.lower() == "k":
        morse.append("-.-")
    elif index.lower() == "l":
        morse.append(".-..")
    elif index.lower() == "m":
        morse.append("--")
    elif index.lower() == "n":
        morse.append("-.")
    elif index.lower() == "o":
        morse.append("---")
    elif index.lower() == "p":
        morse.append(".--.")
    elif index.lower() == "q":
        morse.append("--.-")
    elif index.lower() == "r":
        morse.append(".-.")
    elif index.lower() == "s":
        morse.append("...")
    elif index.lower() == "t":
        morse.append("-")
    elif index.lower() == "u":
        morse.append("..-")
    elif index.lower() == "v":
        morse.append("...-")
    elif index.lower() == "w":
        morse.append(".--")
    elif index.lower() == "x":
        morse.append("-..-")
    elif index.lower() == "y":
        morse.append("-.--")
    elif index.lower() == "z":
        morse.append("--..")
        
for i in morse:
    print(i, end=" ")

```

# Problem Statement 3: ROT13 Cipher

## Submitted Code:

```
string = input()
rot = []
for index in string:
    if index.lower() == "a":
        rot.append("N")
    elif index.lower() == "b":
        rot.append("O")
    elif index.lower() == "c":
        rot.append("P")
    elif index.lower() == "d":
        rot.append("Q")
    elif index.lower() == "e":
        rot.append("R")
    elif index.lower() == "f":
        rot.append("S")
    elif index.lower() == "g":
        rot.append("T")
    elif index.lower() == "h":
        rot.append("U")
    elif index.lower() == "i":
        rot.append("V")
    elif index.lower() == "j":
        rot.append("W")
    elif index.lower() == "k":
        rot.append("X")
    elif index.lower() == "l":
        rot.append("Y")
    elif index.lower() == "m":
        rot.append("Z")
    elif index.lower() == "n":
        rot.append("A")
    elif index.lower() == "o":
        rot.append("B")
    elif index.lower() == "p":
        rot.append("C")
    elif index.lower() == "q":
        rot.append("D")
    elif index.lower() == "r":
        rot.append("E")
    elif index.lower() == "s":
        rot.append("F")
    elif index.lower() == "t":
        rot.append("G")
    elif index.lower() == "u":
        rot.append("H")
    elif index.lower() == "v":
        rot.append("I")
    elif index.lower() == "w":
        rot.append("J")
    elif index.lower() == "x":
        rot.append("K")
    elif index.lower() == "y":
        rot.append("L")
    elif index.lower() == "z":
        rot.append("M")

print("Rot 13 converted Text: ", end="")
for i in rot:
    print(i, end="")


```