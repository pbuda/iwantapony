## Pony is an actor model

- uses actors to run asynchronous code
- passes messages, triggers behaviors
- causal message ordering
- actors are sequential themselves

Note:
Pony uses actors to run asynchronous code. Actors are basically objects that don't provide
synchronous access to their state.

Actors in Pony are light (around 250 bytes of memory overhead).

Idle actors do not use resources except memory.

Data between actors is shared using message passing. Because of the type system
it can be zero-copy passing. Moreover it uses causal ordering.

I can't explain causal ordering well, but it's important. Greg mentioned Lamport's paper and he describes
that there. Causal ordering makes it much easier to run concurrent program.

Actors are sequential which means that code in actor runs sequentially but we can compose actors to achieve
concurrency.

Pony runtime has it's own scheduler (num. threads == num. cores)
