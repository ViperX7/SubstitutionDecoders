# CaesarDecoder
A simple tool to encode/decode text using Caesar and Vigenere with or without key

This tool provides functionality to encrypt or decrypt text using Caesar Cipher
and Vigenere Cipher.
The main purpose of the project is to provide simple programable and extendable
modules to decrypt cypher text without the use of keys or pass phrase

# Features

## Caesar Cipher
    * Normal Encoding Decoding for Alphabets
    * Extended Encoding Decoding using full spectrun of ASCII characterset
    * Shows All Possible Combinations
    * Ability to decode the cypher text and show best guess without any key or password
    * Ability to annalyse any english like writen language and try to decode string
     in that language from an example paragraph great for hinglish styled languages

## Vigenere Cipher
    * Normal Encoding Decoding with the help of the key


# Usage
   
## Caesar
 ```
usage: caesar.py [-h] [-d DECODE] [-e ENCODE] [-k KEY] [-m METHOD]

optional arguments:
  -h, --help            show this help message and exit
  -d DECODE, --decode DECODE
                        Try to decode with(out) key useful if the encoded
                        string has some meaning
  -e ENCODE, --encode ENCODE
                        Encode with the given key
  -k KEY, --key KEY     Supply the key
  -m METHOD, --method METHOD
                        Option to specify encoding/decoding in extended or
                        normal or custom modes default is normal
```

## Vigenere
```
usage: Vigenere_Chipper.py [-h] [-d DECODE] [-e ENCODE] [-k KEY]

optional arguments:
  -h, --help            show this help message and exit
  -d DECODE, --decode DECODE
                        Decode text
  -e ENCODE, --encode ENCODE
                        Encode text
  -k KEY, --key KEY     Key to use for encryption or decryption
```
