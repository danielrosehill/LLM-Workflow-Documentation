---
title: "Prompt library examples"
---

## Basic file sturcture for managing prompt library (markdown)

```
- /drafting
  - /v1.0
    - prompt1.md
    - prompt2.md
  - /v1.1
    - prompt1.md
    - prompt2.md
  - /ideas
    - idea1.md
    - idea2.md

- /production
  - /v1.0
    - prompt1.md
    - prompt2.md
  - /v2.0
    - prompt1.md
    - prompt2.md

- /archived
  - /v1.0
    - prompt1.md (archived)
    - prompt2.md (archived)
  - /v0.9 (pre-production)
    - prompt1.md (archived draft)
    - prompt2.md (archived draft)

- /version-control
  - changelog.md 
  - version-history.md 
 ```   
 
 ## Maintaining version control for developed prompts


 ```
PromptLibrary/
├── Drafts/
│   ├── prompt_v1.md
│   ├── prompt_v2.md
│   └── prompt_v3.md
├── Reviews/
│   ├── review_round_1.md
│   ├── review_round_2.md
│   └── review_round_3.md
├── Final/
│   └── approved_prompt.md
└── Notes/
    ├── feedback_round_1.md
    ├── feedback_round_2.md
    └── feedback_summary.md
 ```   