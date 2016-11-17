## Problems

- we don't know the order of execution
  - atomicity violation
  - order violation
  - deadlocks

Note:
While Programming for concurrency does have it's benefits - it's hard to do properly.
We don't know the order of execution of the tasks so weird things can happen
and finding those issues sometimes is very hard.

Atomicity violation - Concurrent execution is halted and some unknown middle state is set
Two threads do something with an object. One thread checks whether the object is null
and tries to call one of it's methods but it's execution is halted. The second thread
sets the object to null. The first thread resumes and we get a null pointer error.

Order violation is when resource is accessed by more than one thread.
However threads require certain state that might not be achieved when
threads run in different order. Thread one initializes some field
and Thread two assumes it's initialized. But Thread two is fired immediately after creation
before Thread one, so this assumption is wrong and we get error.
Otherwise known as data race

Deadlocks happen when threads wait for other threads to release their locks
So Thread one is holding lock one and waits for lock two to be released.
Thread two is holding lock two but it waits for lock one to be released.
