# CaesarDecoder
A simple tool to encode/decode text using Caesar and Vigenere with or without key

This tool provides functionality to encrypt or decrypt text using Caesar Cipher
and Vigenere Cipher.
The main purpose of the project is to provide simple programable and extendable
modules to decrypt cypher text without the use of keys or pass phrase

## Features

### Caesar Cipher
* Normal Encoding Decoding for Alphabets
* Extended Encoding Decoding using 96 characterset from ascii from ! to ~
      of ASCII characterset that enables it to even decode rot47 chiper
* Shows All Possible Combinations
* Ability to decode the cypher text and show best guess without any key or password
* Ability to annalyse any english like writen language and try to decode string
      in that language from an example paragraph great for hinglish styled languages

### Vigenere Cipher
* Normal Encoding Decoding with the help of the key


## Usage

### Caesar
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

### Vigenere
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
## Limitations in calculating the best guess
The program has only one limitation that exist in accuracy in guessing
and showing the suggested output

* It depends on size of the string for small pieces of text it may give
      false guesses

* By default it is Configured for English it may work for other languages
      too
### Avoiding Limitations
* You are supposed to go through the entire list to see if a better option is
    available

* For any output all possible outputs are shown you can check that
      or you can use the cypher_scorer to train the algorithm for any othere
      language (For training Example have a look at train.py)


## Examples

### Caesar Cipher

* Encoding

    * Normal mode
```
    > ./caesar.py -e "Lets see if it works" -k 22
    Hapo oaa eb ep skngo
```
    * Extended mode Encoding
        In this mode characterset used is changed from a-z A-Z to a subset of
        ASCII characterset  ascii(35) to ascii(126)

```
            > ./caesar.py -e "Lets see if it works" -k 22 -m extended
            b{,+6+{{6!|6!,6/'*#+
```
* Decoding

    * With key

```
            /caesar.py -d "Hapo oaa eb ep skngo" -k 22
            Lets see if it works
```

    * Without key
```
            ./caesar.py -d "Hapo oaa eb ep skngo"
            Hapo oaa eb ep skngo
            Gzon nzz da do rjmfn
            Fynm myy cz cn qilem
            Exml lxx by bm phkdl
            Dwlk kww ax al ogjck
            Cvkj jvv zw zk nfibj
            Buji iuu yv yj mehai
            Atih htt xu xi ldgzh
            Zshg gss wt wh kcfyg
            Yrgf frr vs vg jbexf
            Xqfe eqq ur uf iadwe
            Wped dpp tq te hzcvd
            Vodc coo sp sd gybuc
            Uncb bnn ro rc fxatb
            Tmba amm qn qb ewzsa
            Slaz zll pm pa dvyrz
            Rkzy ykk ol oz cuxqy
            Qjyx xjj nk ny btwpx
            Pixw wii mj mx asvow
            Ohwv vhh li lw zrunv
            Ngvu ugg kh kv yqtmu
            Mfut tff jg ju xpslt
            Lets see if it works
            Kdsr rdd he hs vnqjr
            Jcrq qcc gd gr umpiq
            Ibqp pbb fc fq tlohp

            Best Guess:  Lets see if it works
```

### Vigenere Chipper

* Encoding
```
        > ./Vigenere_Chiper.py -e "Lets see if it works" -k test
        Eill liw by ml phvcl
```
* Decoding
```
        > ./Vigenere_Chiper.py -d "Eill liw by ml phvcl" -k test
        Lets see if it works
```


## Authors

* **Utkarsh Yadav**

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Inspiration : In many CTFs competetion caesar chiper is used. It's useful to have an easy to use option
