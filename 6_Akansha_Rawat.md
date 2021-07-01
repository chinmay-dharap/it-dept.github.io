# Problem Statement 1: Strings in the box

## Submitted Code:

```
def print_in_a_frame(*words):
    size = max(len(word) for word in words)
    print('*' * (size + 4))
    for word in words:
        print('* {:<{}} *'.format(word, size))
    print('*' * (size + 4))
    
print_in_a_frame("I", "Participated", "in", "APSIT", "Codeathon")

```

# Problem Statement 2: English to Morse

## Submitted Code:

```
MCD = { 'A':'.-', 'B':'-...',
        'C':'-.-.', 'D':'-..', 'E':'.',
        'F':'..-.', 'G':'--.', 'H':'....',
        'I':'..', 'J':'.---', 'K':'-.-',
        'L':'.-..', 'M':'--', 'N':'-.',
        'O':'---', 'P':'.--.', 'Q':'--.-',
        'R':'.-.', 'S':'...', 'T':'-',
        'U':'..-', 'V':'...-', 'W':'.--',
        'X':'-..-', 'Y':'-.--', 'Z':'--..'}

def encrypt(msg):
    c = ''
    for word in msg:
        if word != ' ':
            c = c + MCD[word] + ' '
        else:
            c += ' '
    return c

def decrypt(msg):
    msg += ' '
    d = ''
    ct = ''
    for word in msg:
        if (word != ' '):
            i = 0
            ct += word
        else:
            i += 1
            if i == 2 :
                d += ' '
            else:
                d += list(MCD.keys())[list(MCD.values()).index(ct)]
                ct = ''

    return d
def main():
    msg = "school"
    res = encrypt(msg.upper())
    print(res)

    msg = "... -.-. .... --- --- .-.."
    res = decrypt(msg)
    
if __name__ == '__main__':
    main()

```

# Problem Statement 3: ROT13 Cipher

## Submitted Code:

```
dic1 = {'A' : 1, 'B' : 2, 'C' : 3, 'D' : 4, 'E' : 5,
        'F' : 6, 'G' : 7, 'H' : 8, 'I' : 9, 'J' : 10,
        'K' : 11, 'L' : 12, 'M' : 13, 'N' : 14, 'O' : 15,
        'P' : 16, 'Q' : 17, 'R' : 18, 'S' : 19, 'T' : 20,
        'U' : 21, 'V' : 22, 'W' : 23, 'X' : 24, 'Y' : 25, 'Z' : 26}

dic2 = {0 : 'Z', 1 : 'A', 2 : 'B', 3 : 'C', 4 : 'D', 5 : 'E',
        6 : 'F', 7 : 'G', 8 : 'H', 9 : 'I', 10 : 'J',
        11 : 'K', 12 : 'L', 13 : 'M', 14 : 'N', 15 : 'O',
        16 : 'P', 17 : 'Q', 18 : 'R', 19 : 'S', 20 : 'T',
        21 : 'U', 22 : 'V', 23 : 'W', 24 : 'X', 25 : 'Y'}

def et(msg, s):
    c = ''
    for word in msg:
        if(word != ' '):
            x = ( dic1[word] + s ) % 26
            c += dic2[x]
        else:
            c += ' '

    return c

def dt(msg, s):
    d = ''
    for word in msg:
        if(word != ' '):
            x = ( dic1[word] - s + 26) % 26
        else:
            d += ' '

    return d

def main():
    msg = "APSITCODE"
    s = 13
    res = et(msg.upper(), s)
    print("Rot 13 converted Text:", res)

    msg = "NCFVGPBQR"
    s = 13
    res = dt(msg.upper(), s)
    
if __name__ == '__main__':
    main()

```