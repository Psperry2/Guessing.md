   mermaid
   flowchat TD
    A[Random Guessing Game] -->|computer selects range| B((computer selects random number within range))
    B ==> C{{User guesses number}}
    C -.->|Guess is too high| D>Program outputs that the users guess was too high and to guess again]
     D -.-> |User guesses again| C
    C ==>|User guesses correct number| E>Program outputs that user selected the correct number]
    C -.->|Guess is too low| F>Program outputs that the users guess was too low and to guess again]
    F -.-> |User guesses again| C
    E ==> G[\Programs asks if user want to play again/]
    G ==> |User selects yes| B
    G ==> |User selects no| H[Game ends]
       
    ### Flow Chart Description
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