README

This project implements an encryption and decryption system using a circular queue and Fibonacci (Zeckendorf) number representation.

The program works by:

Splitting the input text into chunks based on the chosen queue size.

Storing each chunk inside a circular queue.

Rotating the queue to the left by an amount based on the keyword.

Converting each character in the rotated queue into its Fibonacci representation.

Printing the encrypted Fibonacci sequence.

For decryption, the Fibonacci values are converted back to characters, the queue is reverse-rotated, and the original text is reconstructed.

How the encryption works

Compute start = (sum of ASCII values of letters in keyword) % queueSize.

Take queueSize characters at a time from the text.

Insert them into a circular queue.

Rotate the queue left by 'start' positions.

Convert each character's ASCII value into a Fibonacci representation.

Output these Fibonacci binary strings separated by spaces.

How the decryption works

Split the encrypted Fibonacci binary text by spaces.

Convert each Fibonacci representation back into its ASCII value.

Insert these values into a circular queue.

Rotate the queue left by (chunkSize - start) % chunkSize to reverse the encryption rotation.

Extract characters in order to reconstruct the original text.

Fibonacci Representation

Each character is converted into a Fibonacci-based binary form using Fibonacci numbers:
1, 2, 3, 5, 8, 13, 21, ...
For example, a value like 65 (ASCII for 'A') is represented by selecting Fibonacci numbers that sum to 65.

Program Input

The program asks for:

Text to encrypt

Keyword

Queue size

Program Output

Encrypted Fibonacci binary representation

Decrypted text (should match original)

Notes

Works for all ASCII characters.

Rotation makes the encryption order-dependent.

Fibonacci encoding ensures unusual, non-standard binary output.