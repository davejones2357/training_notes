# Card Entropy

## Setup and usage

update the setup steps to explain typical usage.

Provide explanation of why testdata cannot by fed automatically into the script?

## Error types
In an earlier version, ValueError exceptions were raised only when user input was syntactically invalid—for example, when it could not be interpreted as a playing card. Other invalid operations were classified as RuntimeError.

Instead, problems caused by invalid user-supplied values should also be represented as ValueError, even when the input is syntactically valid. For example, submitting the same card more than once without first indicating that the deck has been reshuffled violates the rules for drawing without replacement and should raise a ValueError subclass.
