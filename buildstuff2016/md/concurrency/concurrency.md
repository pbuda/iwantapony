## Concurrency

- Executing multiple tasks
- Disjoint and overlapping
- Parallel and/or scheduled
- Executed in unknown order

Note:
Let's talk about concurrency. What is it? Do we need it?

The way I think about concurrency is this:

We can split computation into small units or tasks and then execute them in a disjoint
and overlapping way. Those tasks can be scheduled in parallel on multiple processors
or scheduled in arbitrary splices of time on a single processor.

We don't know when each task will be executed relative to other tasks. We have to accept that.

Clarification: Each task is a linear sequence of operations with a well defined order
of execution, however timing of those operations relative to other tasks is unknown.
