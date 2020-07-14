# Hill-Cipher-Cryptography
Implement encryption and decryption using Hill Cipher on variable length plain text. 
The functions of encryption and decryption are well-commented and self-explanatory in the jupyter notebook.

## Hill Cipher
In classical cryptography, the Hill cipher is a polygraphic substitution cipher based on linear algebra. Invented by Lester S. Hill in 1929, it was the first polygraphic cipher in which it was practical (though barely) to operate on more than three symbols at once.
Each letter is represented by a number modulo 26. Though this is not an essential feature of the cipher, this simple scheme is often used:
To encrypt a message, each block of n letters (considered as an n-component vector) is multiplied by an invertible n × n matrix, against modulus 26. To decrypt the message, each block is multiplied by the inverse of the matrix used for encryption.

The matrix used for encryption is the cipher key, and it should be chosen randomly from the set of invertible n × n matrices (modulo 26). The cipher can, of course, be adapted to an alphabet with any number of letters; all arithmetic just needs to be done modulo the number of letters instead of modulo 26.

## Cryptanalysis (Part-2)
Given the ciphertext and length of the key, perform cryptanalysis to find the plain text and the key. 
for a text decrypted through hill cipher.

  ### Introduction
    ● Cryptanalysis of hill cipher is done by assuming that key size is n=2 or n=3.
    ● So, most common bi-grams or tri-grams are used accordingly.
    ● “ Sympy ” library in python is used for the function of modulo-inverse.
    ● Cryptanalysis for both key-size 2 and 3 is done.
    
  ### Cryptanalysis Algorithm Used
   1. Let’s say key K has size, n = 2. Assume a pair of most common di-grams in english.
   2. Make the matrix P, using the most common di-gram pair in english (“th” and “of ”).
   3. Find the most common di-gram pair in cipher text. Make a matrix C
   4. Use the formula, K = C × P<sup>-1</sup> to find the key, K
   5. Find the decrypted plaintext using the key, and the decryption algorithm done in hill_cipher.
   6. If the decryption is not correct then change the di-gram pair in step-2 and repeat.
   7. If analysing using many different di-grams in a loop, use IC of the plaintext as a
    stopping criterion.


