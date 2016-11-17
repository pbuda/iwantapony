## Consuming objects

- consume variables
- destructive read

Note:
Consume variable when you want to move it to another variable

This leaves the old variable empty

No code can use that empty variable unless a new value is written to it

Consuming a variable allows you to make a local alias even for iso and trn

We can consume variables but we can't consume fields

There's another way to move objects - destructive read

It uses the fact that in pony assignment returns the old left-hand side value
and not the newly assigned value

Hard to explain without code, maybe I'll show in examples
