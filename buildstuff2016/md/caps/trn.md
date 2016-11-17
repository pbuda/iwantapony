## Transition - trn

> no other variable can be used by any actor to write to that object, and no other variable can be used by other actors to read from or write to that object

![Trn](md/caps/trn.png)

Note:

This means a trn variable is the only variable anywhere in the program that can write to that object, but other variables held by the the same actor may be able to read from it. It is write unique.

Use trn when you want to be able to change the object for a while but later plan to make it globally immutable (val)
