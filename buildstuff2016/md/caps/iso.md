## Isolated state - iso

> no other variable can be used by any actor to read from or write to that object

![Iso](md/caps/iso.png)

Note:
This means an iso variable is the only variable anywhere in the program that can read from or write to that object. It is read and write unique.

To safely pass data we need to be sure that the actor sending mutable state
gives up it's ability to both read from and write to it.

We can use iso to pass data, because when we do it we effectively are saying
that we're done with it.

If we don't need to pass data, we can use ref instead.
