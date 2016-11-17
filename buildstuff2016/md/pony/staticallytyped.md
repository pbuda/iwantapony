## Pony is statically typed

- it can understand code
- type system makes guarantees
- enforces concurrency patterns
- high performance (llvm)

Note:
Pony is a statically typed, compiled language.

But why it needs to be statically typed? To perform static code analysis during compile
time. This is interesting, because now Pony compiler can make certain guarantees:
- if program compiles, it won't crash
- there will be no unhandled exceptions
- there will never be null dereferences
- there will be no deadlocks or data races
