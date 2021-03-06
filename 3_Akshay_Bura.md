# Problem Statement 1: Strings in the box

## Submitted Code:

```
def apsit_codeathon(*words):

    size = max(len(word) for word in words)
    print('*' * (size + 4))
    for word in words:
        print('* {:<{}} *'.format(word, size))
    print('*' * (size + 4))
    
apsit_codeathon("I","Participated","in","APSIT","Codeathon")

```

# Problem Statement 2: English to Morse

## Submitted Code:

```
MORSE_CODE_DICT = { 'A':'.-', 'B':'-...', 

                    'C':'-.-.', 'D':'-..', 'E':'.', 

                    'F':'..-.', 'G':'--.', 'H':'....', 

                    'I':'..', 'J':'.---', 'K':'-.-', 

                    'L':'.-..', 'M':'--', 'N':'-.', 

                    'O':'---', 'P':'.--.', 'Q':'--.-', 

                    'R':'.-.', 'S':'...', 'T':'-', 

                    'U':'..-', 'V':'...-', 'W':'.--', 

                    'X':'-..-', 'Y':'-.--', 'Z':'--..', 

                    '1':'.----', '2':'..---', '3':'...--', 

                    '4':'....-', '5':'.....', '6':'-....', 

                    '7':'--...', '8':'---..', '9':'----.', 

                    '0':'-----', ', ':'--..--', '.':'.-.-.-', 

                    '?':'..--..', '/':'-..-.', '-':'-....-', 

                    '(':'-.--.', ')':'-.--.-'} 

  

# Function to encrypt the string 

# according to the morse code chart 

def encrypt(message): 

    cipher = '' 

    for letter in message: 

        if letter != ' ': 

  

            # Looks up the dictionary and adds the 

            # correspponding morse code 

            # along with a space to separate 

            # morse codes for different characters 

            cipher += MORSE_CODE_DICT[letter] + ' '

        else: 

            # 1 space indicates different characters 

            # and 2 indicates different words 

            cipher += ' '

  

    return cipher 

  
 





# Hard-coded driver function to run the program 

def main(): 

    message = "School"

    result = encrypt(message.upper()) 

    print (result) 

  


  

# Executes the main function 

if __name__ == '__main__': 

    main() 

```

# Problem Statement 3: ROT13 Cipher

## Submitted Code:

```
dict1 = {'A' : 1, 'B' : 2, 'C' : 3, 'D' : 4, 'E' : 5, 

        'F' : 6, 'G' : 7, 'H' : 8, 'I' : 9, 'J' : 10, 

        'K' : 11, 'L' : 12, 'M' : 13, 'N' : 14, 'O' : 15, 

        'P' : 16, 'Q' : 17, 'R' : 18, 'S' : 19, 'T' : 20, 

        'U' : 21, 'V' : 22, 'W' : 23, 'X' : 24, 'Y' : 25, 'Z' : 26} 

dict2 = {0 : 'Z', 1 : 'A', 2 : 'B', 3 : 'C', 4 : 'D', 5 : 'E', 

        6 : 'F', 7 : 'G', 8 : 'H', 9 : 'I', 10 : 'J', 

        11 : 'K', 12 : 'L', 13 : 'M', 14 : 'N', 15 : 'O', 

        16 : 'P', 17 : 'Q', 18 : 'R', 19 : 'S', 20 : 'T', 

        21 : 'U', 22 : 'V', 23 : 'W', 24 : 'X', 25 : 'Y'} 



def encrypt(message, shift): 

    cipher = '' 

    for letter in message: 

        # checking for space 

        if(letter != ' '): 

            # looks up the dictionary and  

            # adds the shift to the index 

            num = ( dict1[letter] + shift ) % 26

            # looks up the second dictionary for  

            # the shifted alphabets and adds them 

            cipher += dict2[num] 

        else: 

            # adds space 

            cipher += ' '

  

    return cipher 

def main(): 

    # use 'upper()' function to convert any lowercase characters to uppercase 

    message = "APSITCODE"

    shift = 13

    result = encrypt(message.upper(), shift) 

    print ("Rot 13 converted Text:",result) 
    
    



if __name__ == '__main__':

    main()

```