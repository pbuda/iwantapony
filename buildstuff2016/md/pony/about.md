## What is Pony?

- object oriented
- actor model
- type-safe
- no runtime exceptions
- no locks

Note:

Pony has classes and interfaces and traits. Everything is an object and there are no nulls.

It has actors and they can run code asynchronously

It's statically typed

There are no runtime exceptions, all exceptions have defined semantics and have
to be handled properly in the code.

Pony doesn't use locks so it will never deadlock and data races will not happen.
