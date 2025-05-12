# GuitarLang
_A esotaric programming language based on guitar notes_

## Introduction 
All natural notes `A`, `B`, `C`, `D`, `E`, `F` and half-steps `A#`, `C#`, `D#`, `F#`, `G#` used for commands. 
To write a program all notes must be played on a physical guitar and listened to by the interpreter.
Refer to this [guide](https://leadguitarlessons.com/guitar-lessons/general/learn-the-notes-on-the-guitar.htm) for guitar notes on a 6-string.

## Design Principles
- **Readability**: This esolang obsecures the readability of a program so it is harder for a human to immediately interpret. 
- **Ease of programming**: This esolang attempts to make writting programs much more diffcult (but also fun!) as it requires the note to be played on a physical guitar.
- **Coding as an art form**: Can write a program that does something interesting but also sounds good as a song
- **Multi-coding**: The program can double as a song!

## Commands
### Numbers

- **Start with a sign**:
  - `B` = Positive
  - `E` = Negative
- Followed by a binary sequence:
  - `B` = 1
  - `E` = 0
- Ended with `G`

### I/O Commands

| Command | Operation                                  |
|---------|------------------------------------------|
| `EA`    | Read a number from input and push to stack |
| `ED`    | Pop a number and output it as an ASCII character |
| `EG`    | Pop a number and output it directly      |


### Stack Manipulation

| Command | Parameters | Operation                         |
|---------|------------|---------------------------------|
| `AB`    | Number     | Push a number to the stack      |
| `AC`    | -          | Duplicate the top item          |
| `AD`    | -          | Swap the top two items          |
| `AE`    | -          | Discard the top item from stack |


### Arithmetic Operations
Computes operation on top two items on stack and replaces them with the result.

| Command | Operation           |
|---------|-------------------|
| `A#`   | Addition           |
| `C#`   | Subtraction        |
| `D#`   | Multiplication     |
| `F#`   | Integer Division   |
| `G#`   | Modulo             |


### Control Flow

**Labels** are sequences of `B` and `E`, ended with `G`.

| Command | Parameters | Operation                                      |
|---------|------------|----------------------------------------------|
| `GA`    | Label      | Mark a location in the program               |
| `GB`    | Label      | Call a subroutine                            |
| `GC`    | Label      | Jump unconditionally to the label           |
| `GD`    | Label      | Jump to the label if the top stack item is 0 |
| `GE`    | Label      | Jump to the label if the top stack item is negative |
| `GF`    | -          | End subroutine, return to caller             |

## Sample Programs
### Hello World
```
AB B BEEBEEE G ED // 'H'
AB B BBEEBEB G ED // 'e'
AB B BBEBBEE G AC ED ED // 'll'
AB B BBEBBBB G ED // 'o'
AB B BEEEEE G ED  // ' '
AB B BEBEBBB G ED // 'W'
AB B BBEBBBB G ED // 'o'
AB B BBBEEBE G ED // 'r'
AB B BBEBBEE G ED // 'l'
AB B BBEEBEE G ED // 'd'

```
Below is an audio file of this program being played.


https://github.com/user-attachments/assets/4c5eafa8-4f32-4ea7-b94a-cbd622e203cf




## Online Interpreter
TODO (maybe over the summer)
