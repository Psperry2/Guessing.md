```mermaid
flowchart TB
    A[Program selects range] -.- B[Program selects a random number within the range ]
    B ====o |Program prompts user to guess a number within the range| C{{User guesses number}}
       C -.-> |Guess is out of range| D[\Guess was not in range, try again!/]
       D -.-> |User guesses again| C
    C -.->|Guess is too high| E>Guess was too high, try again!]
    E -.- |User guesses again| C
    C -.->|Guess is too low| F>Guess was too low, try again!]
    F -.-> |User guesses again| C
    C ===> |Guess is correct| P[\You guessed correctly!/]
    P -.-> |Would you like to play again?| R[No] 
    R -.-> Q[Game ends]
    P ===> |Would you like to play again?| M[Yes]
    M ==oB
```
    
### Number Guessing Game Flow Chart Description
 1. The program must pick a **random** number within a selected range.
 2. The user is prompted to guess the random number selected by the program
    - **If the user selects a number thats too high.**
        1. The program lets the user know that the value they selected was too high.
        2. The program prompts the user to try again.
    - **If the user selects a number thats too low.**
        1. The program lets the user know that the value they selected was too low.
        2. The program prompts the user to try again.
    - **If the user selects the correct number.**
        1. The program lets the user know that the value they selected was correct.
        2. The program asks the user if they want to play again.
            1. The user selects yes and the program starts over.
            2. The user selects no and the game ends.