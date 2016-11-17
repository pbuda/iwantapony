## Reference capabilities

- express access rights to objects
- type qualifiers
- make concurrency safe

Note:
So objects are capabilities but we need a way to specify access rights to those objects.
Pony does that using reference capabilities.

Reference capabilities tell you what you CAN'T do.

Every object has a type and a reference capability.

Safe concurrency because:
- sharing immutable data
- exchanging isolated data
