## Recovering capabilities

- recovering lifts reference capabilities of the result
- iso, trn, ref can become any
- val, box can become immutable or opaque

Note:
Primarily used to get an iso we can pass to another actor

But allows to create complex mutable data structure and then lift it to val

Borrow an iso i.e. convert it to ref and maybe pass along but in the meantime
modify it and get a new iso afterwards
