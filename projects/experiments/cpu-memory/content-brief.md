# CPU and memory: following one load

**Status:** sourced content draft for a future infographic. Review generated labels and diagrams against these sources before publication.

## Learning goal

Follow one requested value from an instruction to a CPU register. By the end, a learner should be able to explain:

- what the address identifies and what the returned data is;
- how the A-level MAR/MDR and bus model describes a simple memory read;
- why a modern CPU checks caches before main memory;
- what a cache hit, cache miss, and cache line mean.

## The anchor example

Use a RISC-V-style 64-bit load:

```text
x6 = 0x1000
ld x5, 24(x6)
```

The instruction adds the offset `24` to the base address in `x6`, giving effective address `0x1018`. It requests a 64-bit value from that location and places the result in destination register `x5`. For a small worked example, say the value is decimal `42` (`0x2A`). This assembly syntax and address calculation follow Cornell's RISC-V teaching notes; the register names and value are illustrative.

Make the distinction visible:

- **Address `0x1018`:** where the requested bytes are located.
- **Data `42`:** the value returned from those bytes.

## Two useful views of the same idea

### A-level simplified model

The CPU places the target address in the **Memory Address Register (MAR)**. It signals a **read** using the control bus. Memory returns the contents over the data bus into the **Memory Data Register (MDR)**, after which the CPU can move the value into a working register.

This is the familiar Cambridge 9618 teaching model. Label it as a simplified architectural view; MAR and MDR are not a promise that every modern CPU contains two physical registers with exactly these names and boundaries.

### Modern CPU data-load view

The processor computes an effective address and checks the data-cache path. A typical conceptual path is:

```text
destination register ← L1 data cache ← L2 cache ← last-level cache ← memory controller ← DRAM
```

The levels and sharing arrangements vary between processor designs. On a hit, a nearby cache supplies the requested value. On a miss, the request continues to a lower level. If it reaches DRAM, the memory system commonly transfers a cache line containing the requested address; the CPU selects the requested bytes and makes them available to the instruction. The line size and exact transfer behavior depend on the design.

For a more advanced margin note, programs commonly use virtual addresses. A data TLB helps translate an address before the physical memory system is accessed. Keep this outside the main path so it adds depth without obscuring the core explanation.

## Why the cache line matters

A load may ask for one byte, word, or doubleword, while a cache transfers a larger block. That block is called a **cache line**. It brings nearby bytes along because programs often access neighboring locations soon after one another. This is spatial locality. Reusing the same value soon is temporal locality.

Use an abstract strip of neighboring byte cells and label it “one cache line — size depends on the processor.” Avoid assigning a universal byte count.

## Performance takeaway

Registers are very small and close to the execution core. Caches provide smaller, faster storage than DRAM and hold copies of recently or nearby used data. DRAM supplies much larger working storage, with higher access latency. The hierarchy balances speed, capacity, and cost.

Do not put fixed access-time or cache-capacity numbers in this first visual. Those depend on processor generation, memory configuration, and workload. A later performance infographic can use a clearly named example CPU and sourced measurements.

## A useful boundary

An ordinary load instruction follows the processor's memory system. SSD storage is not simply another cache level in the L1 → L2 → DRAM lookup path. The operating system and I/O mechanisms move data between persistent storage and RAM when needed; the load then accesses the process's memory through the processor's address-translation and cache machinery.

## Suggested headline and closing line

**Headline:** One load. A long trip.

**Subtitle:** How a CPU retrieves a value from memory.

**Closing line:** A load names one address. The memory hierarchy tries the closest copy first.

## Sources

- [Cambridge International AS & A Level Computer Science 9618 syllabus for 2026](https://www.cambridgeinternational.org/Images/697372-2026-syllabus.pdf) — MAR, MDR, PC, buses, cache memory, and the fetch-execute cycle are included in the stated learning objectives.
- [Cornell CS 3410: Load & Store](https://www.cs.cornell.edu/courses/cs3410/2024fa/notes/asm-mem.html) — RISC-V load syntax, effective address calculation, load width, and the memory-hierarchy trade-off.
- [Cornell CS 3410: Caches](https://www.cs.cornell.edu/courses/cs3410/2024fa/notes/caches.html) — cache blocks/lines, spatial locality, hit/miss behavior, and multi-level caches.
- [OpenStax: Computer Systems Organization](https://openstax.org/books/introduction-computer-science/pages/5-1-computer-systems-organization) — a general CPU overview covering instruction fetch/decode/execute, registers, ALU, cache, memory controller, and the role of RAM.
- [Intel: Memory Performance in a Nutshell](https://www.intel.com/content/www/us/en/developer/articles/technical/memory-performance-in-a-nutshell.html) — one vendor's description of private/shared caches and main memory; used only to support the caveat that actual hierarchies vary.
