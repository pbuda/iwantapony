# Summary

- we want concurrency but it's hard to do right
- Pony can help with that

![Capabilities FTW](md/capabilities_ftw.jpg)

Note:
We want to make our code concurrent ready (because scalability and efficiency)

Doing so is hard, but we have patterns for dealing with problems

Pony uses those patterns and helps us creating concurrency safe, lock-less, data-race free
programs that will not throw runtime exceptions.

To do so Pony uses reference capabilities.
