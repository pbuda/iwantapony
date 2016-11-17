## Capability aliasing

- more than one variable pointing to the same object
- iso > tag
- trn > box
- everything else as itself
- ephemereal types (iso^)
- alias types (iso!)

Note:
What counts as aliasing? Assigning value to a variable and passing a value as an
argument to the method.

Iso can be aliased to a tag because our original reference is the only
reference that can read/write to that object. Tag prevents that, so we're safe.

Trn can be aliased as box because we have to prevent our alias from writing
but at the same time allow original trn to continue writing. Box is just for that.

ephemereal types are used when we consume a variable but we haven't given it a name yet
like returning consume from a method. This is necessary because we can return something that
is not possible to alias that thing. So we use dash to indicate such situation.

Alias type is just saying: whatever we can safely aliast this thing as. Mainly used in generics.
