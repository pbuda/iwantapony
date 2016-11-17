## Value - val

> no other variable can be used by any actor to write to that object.

![Val](md/caps/val.png)

Note:
This means that the object can't ever change. It is globally immutable.

This is a sendable capability, because it guarantees that no actor will ever write
to that object.
