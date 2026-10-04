# Visual brief: one CPU load

Use the approved brand style in [STYLE.md](../../../docs/STYLE.md).

## Audience and purpose

For A-level and introductory university learners. Explain one data-load operation, connecting the simplified bus model students may meet in class with the cache path in a modern processor.

## Main claim

A load instruction names a memory address. The CPU checks nearby cached copies first and uses the returned data in a register.

## Composition

- Use the light paper canvas, shared semantic palette, editorial serif heading, precise linework, and explanatory density from the brand guide.
- Make the central visual a large CPU-to-memory cutaway: register file, L1 data cache, L2 cache, last-level cache, memory controller, and DRAM.
- Show the address request moving through the cache path and the requested data returning to the destination register.
- Make the cache-hit route short; show a cache miss continuing to lower levels and, when needed, DRAM.
- Start the reading path with the code example and its effective address.
- Add an inset that maps the same read to the A-level MAR, MDR, address bus, data bus, and control bus model.
- Add supporting details for address versus data, a cache line containing neighboring bytes, and the speed/capacity trade-off.
- Put virtual-address translation in a small university extension outside the main reading path.

## Copy and example values

- `ld x5, 24(x6)`
- `x6 = 0x1000`
- `effective address = 0x1018`
- `requested value = 42 (0x2A)`
- `ADDRESS = WHERE`
- `DATA = WHAT`
- `CACHE HIT` / `CACHE MISS`
- `L1 DATA CACHE` / `L2 CACHE` / `LAST-LEVEL CACHE` / `MEMORY CONTROLLER` / `DRAM`
- `MAR` / `MDR` / `ADDRESS BUS` / `DATA BUS` / `CONTROL BUS`
- `One load names one address. The memory hierarchy tries the closest copy first.`

## Accuracy checks

- Keep CPU registers distinct from cache levels.
- Label the MAR/MDR route as a simplified teaching model, not a claim about the internal registers of every modern CPU.
- Keep the address `0x1018` distinct from the returned data `42`.
- A cache line contains neighboring bytes; do not assign a universal size.
- Do not add fixed cache capacities or access times without a named processor and a supporting source.
- SSD storage is not another level in the CPU's cache lookup path.
