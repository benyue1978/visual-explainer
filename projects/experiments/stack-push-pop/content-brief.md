# Stack: push, pop, and the top

**Audience:** A-level and introductory university learners.  
**Complexity:** Introductory.  
**Status:** sourced visual content draft.

## Learning objective

Explain how a stack's `push`, `pop`, and `peek` operations act on its top, and predict the order in which values leave the stack.

## Main claim

A stack only adds and removes items at its top, so the last item pushed is the first one popped: last in, first out (LIFO).

## Worked example

Start empty and run:

```text
push(12)
push(7)
pop()     → returns 7
push(5)
```

Final stack, bottom to top: `12, 5`. The next `pop()` returns `5`; after that, `pop()` returns `12`.

## Core operations

- **PUSH(value):** add a value at the top.
- **POP():** remove and return the top value.
- **PEEK():** read the top value without removing it.
- **TOP:** the only end directly available through the stack abstraction.

## Supporting details

- Popping an empty stack is an **underflow** condition; an implementation can report an error or define another handling rule.
- Pushing past capacity is an **overflow** only for a bounded implementation that cannot grow. A growable implementation may resize instead.
- A stack is an abstract data type; it can be implemented with an array or linked nodes. The LIFO behavior does not depend on that choice.
- A program's call stack is a related use: nested calls return in reverse order. Keep this as a short application note rather than equating every stack with the runtime call stack.

## Misconceptions and boundaries

- A stack is not “last item at the bottom”; the top is the end where push and pop occur.
- `PEEK` does not remove the item.
- LIFO defines the access rule, not the physical layout or a single required implementation.
- Underflow and overflow handling can depend on the implementation or language.

## Exact learner-facing copy

- `A stack works from one end: the top.`
- `PUSH adds to the top.`
- `POP removes and returns the top.`
- `PEEK reads the top; it stays there.`
- `Last in, first out (LIFO)`
- `push 12 → push 7 → pop returns 7 → push 5`
- `UNDERFLOW: pop an empty stack`
- `OVERFLOW: only when a fixed capacity is full`
- `Array or linked nodes: same stack behavior`
- `Nested calls return in reverse order.`

## Sources

- [OpenDSA: Stacks and Queues](https://opendsa-server.cs.vt.edu/ODSA/Books/CSC201F26notes/html/StackQueue.html) — LIFO, top, and push/pop definitions.
- [OpenDSA: Stacks](https://opendsa-server.cs.vt.edu/ODSA/Books/umw/cpsc340/fall-2024/CPSC340_F24/html/StackArray.html) — stack operations, array-based and linked implementations, and common applications.
- [OpenDSA: Stack interface](https://opendsa-server.cs.vt.edu/ODSA/Books/ucsc/cse101/spring-2025/CSE101P/html/ContentStacks.html) — push, pop, peek, and the empty-stack precondition for pop.
