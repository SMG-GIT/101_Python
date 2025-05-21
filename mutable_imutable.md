## Mutability and Immutability in Python

*In Python, every variable holds a reference (memory address) to an object. Objects are either mutable or immutable, defining whether their value can change after creation.*

**1. Immutable Objects:**

> **Definition:** Their value cannot be changed in-place. 
Any operation that seems to modify them (like adding to a string or number) actually creates **a brand new object** in memory, and the variable's reference is updated to point to this new object.

**Examples:** int, float, str, tuple, bool, frozenset.

**Memory Impact:** The id() (memory address) of an immutable variable changes if its value is "modified."

**Use Cases:** Can be used as dictionary keys or set elements because their hash value is constant.

**2. Mutable Objects:**

>**Definition:** Their value can be changed in-place after creation without creating a new object. Operations directly alter the object's contents at its existing memory location.

**Examples:** list, dict, set.

**Memory Impact:** The id() (memory address) of a mutable variable remains the same even after its contents are modified.

**Use Cases:** Cannot be used as dictionary keys or set elements because their value (and thus hash) can change.

**Key Implications:**

**Function Arguments:** Modifying a mutable object passed to a function will affect the original object outside the function. Modifying an immutable object in a function will only create a new local object, leaving the original untouched.

**Default Arguments:** Using mutable objects as default function arguments can lead to unexpected shared state across function calls.

**Aliasing:** Multiple variables can refer to the same mutable object, meaning changes through one variable are visible through all others.*
