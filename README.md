# Caesar-cipher
#python code for caesar cipher

message = "This is my secret message."

key = 13 # the encryption/decryption key

mode = "encrypt" # tells the program to encrypt or decrypt

LETTERS = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"

translated = "" # stores the encrypte/decrypted message

message = message.upper()

for symbol in messages:
    if symbol in LETTERS:
        num = LETTERS.find(symbol) # get the number of the symbol
        if mode == "encrypt":
            num += key
        elif mode == "decrypt":
            num -= key
        # LETTERS or less than 0
        if num >= len(LETTERS):
            num = num - len(LETTERS)
        elif num < 0:
            num = num + len(LETTERS)
   
        translated = translated + LETTERS[num] # add encrypted/decrypted number's symbol at the end of the translated
    else:
        translated = translated + symbol

print(translated)
    
   
      
