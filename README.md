# Visual CS

Visual CS is a docs-first studio for clear visual explanations. Its shared brand serves A-level and university learners, as well as software professionals working with topics such as AI testing and AI engineering.

## Guides

| Document | Purpose |
|---|---|
| [STYLE.md](docs/STYLE.md) | Approved brand identity: palette, canvas, typography, illustration, composition, and the reusable infographic style anchor. |
| [EXPLANATION_GUIDE.md](docs/EXPLANATION_GUIDE.md) | How to build an accurate learner mental model and explain a mechanism clearly. |
| [CONTENT_GUIDE.md](docs/CONTENT_GUIDE.md) | How to research a topic, prepare a sourced content brief, and check the example and claims. |
| [CONTENT_BRIEF_TEMPLATE.md](docs/CONTENT_BRIEF_TEMPLATE.md) | Reusable structure for research and explanation briefs across topics. |
| [INFOGRAPHIC_GUIDE.md](docs/INFOGRAPHIC_GUIDE.md) | The end-to-end process for planning, generating, reviewing, and exporting an infographic. |
| [IMAGE_PROMPT_GUIDE.md](docs/IMAGE_PROMPT_GUIDE.md) | Reusable image-prompt structure, style-reference instruction, iteration, and visual QA. |
| [VIDEO_GUIDE.md](docs/VIDEO_GUIDE.md) | Video production stages, tool roles, narration, alignment, captions, rendering, and QA. |
| [WORKFLOW.md](docs/WORKFLOW.md) | How the guides and tools fit together from topic selection through final output. |

Use `WORKFLOW.md` as the starting point. The relevant guide contains the detailed steps and reusable prompts.

## Projects

Create production work in `projects/<topic>/`, using a content brief, visual brief, prompt or script, final output, publishing copy, and review notes as appropriate. The maintained [Data Representation series](projects/data-representation/README.md) is the current example of this structure. Add project-specific code only when a deliverable needs it; extract shared code after a pattern has proved useful across projects.

## Repository structure

```text
visual-cs/
├── docs/                 # reusable brand, content, prompt, and production guides
└── projects/
    └── <topic>/          # production topic projects
```
