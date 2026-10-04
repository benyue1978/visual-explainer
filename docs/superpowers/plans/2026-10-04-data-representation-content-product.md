# Data Representation Content Product Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [x]`) syntax for tracking.

**Goal:** Build the written content package for the Data Representation learning series around concepts and explanations, with an internal concept-level completeness review and an intentionally open infographic count.

**Architecture:** Keep the product materials together in `projects/data-representation/`: an entry point, an internal coverage matrix, a candidate catalogue, traceable textbook reference notes, and a reusable content-brief template. Treat the approved design spec and repository guides as the source of truth; use syllabus documents only to spot concept-family gaps, never to define the learner-facing sequence or image labels.

**Tech Stack:** Markdown; repository content and explanation guides; Cambridge 0478 and 9618 documents as internal coverage references; no code or image assets in this phase.

---

## File map

- `projects/data-representation/README.md` — product purpose, intended learner, prior knowledge, six-module concept path, links to package files, and current decisions.
- `projects/data-representation/coverage-matrix.md` — internal review of concept families, where they are explained, cross-module links, and open checks; not a syllabus-objective mapping.
- `projects/data-representation/infographic-catalogue.md` — candidate learning pieces and example seeds; does not set a final image count.
- `projects/data-representation/textbook-reference-notes.md` — what is and is not verifiable about the mentioned textbook material, plus the adaptation record format.
- `docs/CONTENT_BRIEF_TEMPLATE.md` — reusable research and explanation brief aligned with `docs/CONTENT_GUIDE.md`.

## Task 1: Create the product entry point

**Files:**
- Create: `projects/data-representation/README.md`

- [x] **Step 1: Create the directory and add the product overview**

  State the product promise: teach how bits represent, encode, calculate, store, and compress information. Name the audience as IGCSE and AS/A Level Computer Science learners and their teachers. State prior knowledge (decimal place value and integer arithmetic) and that the series introduces bits and binary from the beginning.

- [x] **Step 2: Record the six-module concept path**

  List, in order: Bits, Bytes & Magnitudes; Representing Numbers; Representing Text; Representing Images; Representing Sound; Storage & Compression. Give each one its learner question and one sentence explaining its connection to the next module, or how the final module brings earlier ideas together. Preserve the shared `01000001` opener as a teaching device that can sit inside the first piece; do not make it a mandatory standalone poster.

- [x] **Step 3: Record the working rules and link the package**

  State that infographic count is undecided; the catalogue contains candidates only. State that any internal completeness check is concept-level, while learner-facing art contains no syllabus name/code, exam year, section number, level badge, or coverage marker. Link the other four package files and the repository's content, explanation, infographic, and workflow guides using working relative links.

- [x] **Step 4: Commit the entry point**

  Run: `git add projects/data-representation/README.md && git commit -m "docs: add data representation product overview"`

## Task 2: Build the internal concept-family coverage matrix

**Files:**
- Create: `projects/data-representation/coverage-matrix.md`

- [x] **Step 1: Add the matrix scope note and columns**

  Explain at the top that this is an editorial completeness aid, not a public syllabus map. Use columns for concept family, knowledge to explain, primary module, connections to other modules, and editorial check/source note. Do not create one row per examination objective or a column for syllabus year, paper, or outcome code.

- [x] **Step 2: Add the eight concept families from the approved design**

  Include: digital foundations and capacity; integer and numeric representation; arithmetic and bit manipulation; floating-point representation; text encoding; image representation; sound representation; file size and compression. Preserve the specific knowledge and misconception checks listed in Section 4 of `docs/superpowers/specs/2026-10-04-data-representation-design.md`.

- [x] **Step 3: Record internal source metadata and unresolved checks**

  Use the official source links already recorded in the approved spec only as broad scope sanity references. The purpose is to catch a missing concept family, not to check a specific syllabus year: do not compare editions, track year-specific changes, create examination-objective rows, or use syllabus codes, years, or sections as matrix dimensions. Mark checks as “review needed” wherever a future worked example, terminology choice, implementation detail, or source claim needs validation.

- [x] **Step 4: Commit the matrix**

  Run: `git add projects/data-representation/coverage-matrix.md && git commit -m "docs: add concept coverage review for data representation"`

## Task 3: Turn the catalogue into a decision-ready candidate list

**Files:**
- Create: `projects/data-representation/infographic-catalogue.md`

- [x] **Step 1: Add the open-count rule and selection criteria**

  State clearly that the entries are candidate explanations, not a promised count. Choose whether to combine or split only after checking that each resulting piece has one teachable question, enough room for a complete worked example at the intended reading size, a clear scope boundary, and a useful connection to the sequence.

- [x] **Step 2: Add all thirteen candidate entries**

  Include the candidates from Section 5 of the approved spec: bits and capacity; one value in several bases; signed integers and integer arithmetic; BCD; bit manipulation; floating point; text; bitmap images; vector graphics; sound; file size; lossless compression; lossy compression. For every entry include a learner question, explanation mechanism or claim, worked-example seed, likely confusion/boundary, module link, and status `Candidate`.

- [x] **Step 3: Preserve the worked-example seeds and their limits**

  Copy the approved seeds accurately, including their conditions and units. Keep seeds visibly distinct from reviewed examples: formal briefs still need exact inputs, intermediate states, result, units, and a source or transparent derivation. Label teaching formats and simplified cases, such as the small floating-point format and compression payload examples, as illustrative where applicable.

- [x] **Step 4: Commit the candidate catalogue**

  Run: `git add projects/data-representation/infographic-catalogue.md && git commit -m "docs: add data representation candidate catalogue"`

## Task 4: Create traceable textbook reference notes

**Files:**
- Create: `projects/data-representation/textbook-reference-notes.md`

- [x] **Step 1: State what source material is available**

  Record that the supplied text mentions textbook material and explicitly describes a binary/decimal-prefix comparison, but the screenshots, book title, edition, page numbers, and figure numbers were not supplied. Do not claim to have inspected images or invent bibliographic details.

- [x] **Step 2: Separate confirmed description from unverified leads**

  Record the prefix comparison as a description present in the supplied text. Put pixel zoom, wave sampling, bit boxes, registers, file-size flow, and RLE under “textual leads to verify,” not “observed in screenshot.” For each entry include evidence currently available, concept it may help explain, what must be checked against the original, and how Visual CS will reinterpret it.

- [x] **Step 3: Add a reusable reference-record format**

  Include fields for book/title, edition, chapter, page/figure, source artifact received, observed teaching move, concept served, limits or simplifications, Visual CS adaptation, asset/licensing note, and verification status. Allow unknown fields to be marked “not provided.”

- [x] **Step 4: Commit the reference notes**

  Run: `git add projects/data-representation/textbook-reference-notes.md && git commit -m "docs: record data representation textbook references"`

## Task 5: Add a reusable content-brief template

**Files:**
- Create: `docs/CONTENT_BRIEF_TEMPLATE.md`

- [x] **Step 1: Create the learner and scope fields**

  Include fields for audience and prior knowledge, learner question/objective, scope, exclusions, main claim, and links to neighboring concepts. Keep the internal working language flexible; learner-facing copy can default to English for the intended audience.

- [x] **Step 2: Create the explanation and evidence fields**

  Include a mechanism model (objects, inputs, state changes, outputs, causal steps), one traceable worked example, supporting distinctions or boundary cases, common misconceptions and corrections, terminology, simplifications or implementation differences, and direct sources beside the claims they support.

- [x] **Step 3: Add local quality checks**

  Require worked examples to identify exact inputs, intermediate steps, outputs, and unit handling. Require the author to distinguish sourced facts, transparent derivations, teaching abstractions, and implementation-dependent behavior. Add an explicit check that examination metadata and coverage labels stay out of learner-facing art. Do not add layout or image-prompt fields to this content template; those belong in a later visual brief.

- [x] **Step 4: Commit the brief template**

  Run: `git add docs/CONTENT_BRIEF_TEMPLATE.md && git commit -m "docs: add data representation content brief template"`

## Task 6: Review the package against the approved design and repository guides

**Files:**
- Review: `projects/data-representation/README.md`
- Review: `projects/data-representation/coverage-matrix.md`
- Review: `projects/data-representation/infographic-catalogue.md`
- Review: `projects/data-representation/textbook-reference-notes.md`
- Review: `docs/CONTENT_BRIEF_TEMPLATE.md`
- Reference: `docs/superpowers/specs/2026-10-04-data-representation-design.md`
- Reference: `docs/CONTENT_GUIDE.md`, `docs/EXPLANATION_GUIDE.md`, `docs/INFOGRAPHIC_GUIDE.md`, and `docs/WORKFLOW.md`

- [x] **Step 1: Check design coverage and count policy**

  Confirm the package retains all six modules, all thirteen candidates, all eight concept families, the shared `01000001` opener, the knowledge-first sequence, and the rule that image count remains open. Confirm no exact syllabus-objective mapping has been introduced.

- [x] **Step 2: Check examples and reference provenance**

  Recalculate each numeric seed in the catalogue, check that units and stated assumptions remain present, and mark any seed needing an authoritative source before it becomes a formal brief. Confirm textbook observations and unverified leads are clearly separated and no absent screenshot, book detail, or page number has been fabricated.

- [x] **Step 3: Check learner-facing constraints and links**

  Review every package file for syllabus metadata intended for artwork, ensure the exclusion rule is explicit, and follow each relative Markdown link to verify its target exists. Run `git diff --check c46ccf6..HEAD`; expected result is no whitespace errors across the package commits. Do not add or run software tests for this documentation-only package.

- [x] **Step 4: Fix review findings and commit the finished package**

  Make any corrections directly in the responsible file, then stage them with `git add projects/data-representation` and run `git diff --cached --check`; expected result is no whitespace errors. Run `git status --short`. If review corrections were needed, commit them with `git commit -m "docs: review data representation content package"`; if there were no corrections, do not create an empty commit.

## Completion criteria

- The five files in the file map exist and link to one another where useful.
- The six-module route is organized by ideas and learning dependencies.
- The catalogue contains thirteen candidates while leaving the final infographic count undecided.
- Completeness checks remain internal and concept-level; no learner-facing syllabus labels or coverage marks are specified.
- The textbook notes accurately distinguish supplied descriptions from material that has not been seen.
- Every example seed is either arithmetically checked or explicitly marked for further source review before formal publication.
- No infographic or first-image prompt is created in this phase.
