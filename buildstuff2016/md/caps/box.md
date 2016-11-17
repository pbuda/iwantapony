## Box

> no other variable can be used by other actors to write to that object

![Box](md/caps/box.png)

Note:
This means that other actors may be able to read the object and other variables in the same actor may be able to write to it (although not both). In either case it is safe for us to read. The object is locally immutable.

In other words, you can use box when you don't care whether object is mutable or not - you
want to read from it but don't want to write to it or share it.

This is useful because you can write code that will work for both vals and refs.

Your function can accept box variable and when you call it you can use val or ref variable
(capability subtyping)
