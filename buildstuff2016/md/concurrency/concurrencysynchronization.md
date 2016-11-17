## Synchronization

- govern access to shared resource
- solves problems
- can lead to no concurrency at all

Note:
Synchronization is a concept of governing access to a shared resource by using locks.
When more than one thread wants to access the resource, we can tell them to wait
for their turn.

This effectively helps dealing with atomicity and order violation issues,
but can introduce other problems itself, like starvation or busy waiting (When
checking for access can take time of execution from other threads)

But using synchronization removes concurrency - one thread can access data
so other threads have to wait.

This can be really problematic in languages which have one, global lock - it removes
all concurrency because all threads have to wait for access.

We can fix this by using fine grained synchronization, such that only really critical
parts of the program are synchronized. But this leads to increased cognitive complexity
as reasoning about all the synchronized parts can be hard.
