## Immutable state

- data can't change
- can share global state
- can't migrate without copy
- doesn't work when you need to change state

Note:
Sharing mutable data is problematic, so let's not allow modification of our data
by other threads.

This works well, but has it's own problems:
when you work on some piece of data, you have to make a copy of it, change it and
then share immutable state again.
