## Isolated state

- exclusive access to state
- ony one task can change data
- sharing over time
- no concurrent access

Note:
We can make data accessible only from one place at a time.
This means that only one thread can write and read that data.

This isn't possible in parallel, because you can only have one reference to
the isolated state, so it removes parallel concurrency. However we can share this data
safely over time, i.e. when one task is done with data it can pass it to another.

So isolated data is not shared, but passed.

So what would we like to have in a tool that helps us write safe concurrent code?

I'd expect the tool to help me with using those safe patterns, so that it supports them
and checks whether they are properly used. I'd like to make those checks during compile time
so I don't get errors once app is in production sometime later.

And of course I'd like to have a clean syntax for that.
