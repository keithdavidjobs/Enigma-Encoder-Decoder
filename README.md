# Enigma-Encoder-Decoder
A basic implementation of an Enigma machine with both encode and decode capabilities. Written in Swift AND Javascript.

# Background

The enigma machine was a rotary based cipher machine used in the early 1900s by the Germans.
But it was based on a rotar-cipher machine that was invented simultaneusly around the world.
This machine has its most notable appearance in the hit movie The Imitation Game, where Alan Turing and Joan Clarke are responsible for cracking the algorithm to decode encrypted messages.

## How it works (A very basic and simplified version)
[Shortcut video to see how it works - (explanation begins at 2:04)](https://www.youtube.com/watch?v=ASfAPOiq_eQ)
* There are 3 rotars.
* Each rotar has 26 inputs (representing the letters of the alphabet) that maps to 26 outputs (also representing the letters of the alphabet). The inputs and outputs of these rotars are randomized in a predetermined way. 
* There are 26 keys on the keyboard (only the letters in the alphabet).
  * When a key is pressed, it sends a signal to the corresponding input of the first rotar. The first rotar then outputs 1 of the 26 letter outputs that is mapped to the input.
  * The output from the first rotar is the input to the second rotar, which then produces an output that goes to the 3rd rotar, which produces a final output for the decoded message.
  * **IMPORTANT:** Here's what makes the machine strong. After rotar 3 gives us the final output, the first rotar moves 1 click. Think of this like the odometer on your car or a rotary clock. You have multiple rotars and the one on the far left side moves 1 unit after some distance or some amount of time. When one rotar makes a complete revolution, the next rotar then moves forward one click as well. This repeats until all the rotars have reset to their initial position.
  
## Challenge
Build an encoder and decoder using the Enigma algorithm.

## Solution
1. Make 3 arrays (or dictionaries/hashtables - if you want to be more accurate) to represent the rotars. Each array should contain some made up **UNMUTABLE** random order of the 26 letters in the alphabet. (lets only handle lowercase letters)
2. Using [Ascii](http://www.asciitable.com/) we can represent the letters a-z as an interger between 97-122.
