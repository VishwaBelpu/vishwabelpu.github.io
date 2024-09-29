#vishwabelpu.github.io
```mermaid

flowchart TD
    Start([Start]) --> NewInput
    NewInput --> Match(("Does this guess match the number?"))
    Match -- Yes --> Win{{"Congratulations, you win!"}}
    Match -- No --> Check{"Higher or Lower?"}
    Check -- Higher --> HigherRetry["Feedback: your number is too low!"]
    Check -- Lower --> LowerRetry["Feedback: your number is too high!"]
    HigherRetry --> Retry["Would you like another guess?"]
    LowerRetry --> Retry["Would you like another guess?"]
    Retry --> NewInput

%% Start([Start]) --> gives us the start to the game and is meant to start the game when a new input is put in the textbox
%% NewInput --> Match (("Does this guess match the number?")) is meant to check if the guess is correct. If match registers the number to be different, it will send it to the check function
%% The Check function will see the input that the player provided and will give feeback on whether the input is too high or too low, depending on what the number is.
%% After providing feedback on the guess, it procceeds to go to HigherRetry or LowerRetry, where both will go back to the Retry function that allows the player to keep guessing until they get the right number.