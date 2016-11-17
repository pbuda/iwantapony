## Subtyping

- sometimes we need to supply other types
- we need to make sure we can do that safely
- simple substitution
- aliased and ephemeral substitution

![Transitive](md/caps/transitive.png)

Note:
Sometimes we need to provide other reference capability than we actually have
(like when passing arguments to a function).
So subtyping is telling us what reference capabilities we can provide in which cases.

An iso is read and write unique, and a trn is just write unique, so it's safe to substitute an iso for a trn.

A trn is mutable and also write unique. A ref is mutable, but makes no uniqueness guarantees. It's safe to substitute a trn for a ref.

A trn is write unique and a val is globally immutable, so why is it safe to substitute a trn for a val? The key is that, in order to do so, you have to give up the trn you have. If you give up the only variable that can write to an object, you know that no variable can write to it. That means it's safe to consider it globally immutable.

A ref guarantees no other actor can read from or write to the object. A box just guarantees no other actor can write to the object, so it's safe to substitute a ref for a box.

A val guarantees no actor, not even this one, can write to the object. A box just guarantees no other actor can write to the object, so it's safe to substitute a val for a box.

A box guarantees no other actor can write to the object, and a tag makes no guarantees at all, so it's safe to substitute a box for a tag.

Subtyping is transitive. That means that since iso <: trn and trn <: ref and ref <: box, we also get iso <: box.

There are rules also for aliased and ephemeral types but I won't cover that, sorry
