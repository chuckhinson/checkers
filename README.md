# checkers
This repository is where I keep all the files for my checkers engine. The goal is to create a program that can play checkers and win every time against any human.

## General Plan of Attack:

- [x] represent the relevant board information as an ordered list of bitmaps

- [ ] create a move finder for each of the following types of moves:
    - [x] **simple move:** a move from one square to an empty neighboring square which is immediately diagonal to the starting square
    - [ ] **jump move:** a move from one square to another square that is two diagonal squares in the same direction away from the initial square; the first diagonal square in the path must contain an opposite colored piece (which is then captured), and the destination square must be empty; jumps can also occur in chains (and they must continue jumping if possible), meaning if another jump is possible after an initial jump, then the jumping piece must continue jumping in that direction

- [ ] create an evaluation function to evaluate any board position and find the best move from a list of all possible moves in that position (up to a reasonable depth)

- [ ] create a player input method that will alow a person to play a game of checkers against the engine

---

> **Note:** I am attempting to do as much of the problem solving on my own in terms of best practices for coding the ideal checkers engine. (Eg. For finding jump moves for regular pieces, I know I can just create a binary tree since they only ever have two possible jump options at a time. When it comes to king pieces, though, I will attempt to create my own data structure and algorithm to find all possible jump moves since they can jump in four directions at a time.) However, I will obviously turn to the internet for help if I hit a wall.