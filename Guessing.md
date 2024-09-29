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
