---
title: "Prompt Storage: Recommendations"
---

## Prompt storage, versioning, management

As mentioned in `files-and-folders`, while the idea of storing and managing LLM outputs is a bit less popular, the idea of formally storing and managing LLM prompts is a good deal more established - thanks, probably, to the fact that LLM prompt engineering is already an established discipline (whereas the idea that their outputs should be managed stil raises some eyebrows!)

## Example prompt folder structure using markdown

Before we get to why you might *not* wish to use markdown, here's an example prompt storage folder structure written *using* markdown.

Personally, I store almost everything to do with working with LLMs as markdown (outputs, readable docs) or Python (because .... what *can't* Python do!?)

It's lightweight and has the major advantage that - alongside LLMs themselves - it's becoming increasingly supported by mainstream tools such as Google Drive.

Prompting can be a great collaborative process and keeping a prompt library in markdown affords quite a bit of versatility if using several platforms together.

 ```markdown
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

## Using JSON for prompt storage

It's also possible to use JSON to structure your prompts and makes particular sense if:

- You're storing parametric data in addition to the raw text of the prompt  
- You're integrating your prompt library into a database or any formal data management sytem (or plan to in the near future)

 ```json
{
  "id": "001",
  "title": "Summarize a News Article",
  "description": "This prompt asks the model to summarize a given news article into a concise paragraph.",
  "prompt": "Summarize the following news article in one paragraph: {{article_text}}",
  "tags": ["summarization", "news", "concise"],
  "author": "Perplexity AI",
  "created_at": "2024-11-20T13:00:00Z",
  "last_updated": "2024-11-20T13:00:00Z"
}
```

## Versioning prompts

One of the most useful reasons to store prompts in a structured library is that you can maintain versions of prompts, iterate through them, and (assuming you're recording the outputs) see how different prompts did.

In my opinion (I accept that it is only that) while version control is excellent (and I use Git for all my LLM projects), it's better to preserve the individual versions than to rely on trying to use the VCS to roll back individual files. 

For that reason (and because did I mention text is light on storage?!) I record iterations of prompts as I go through them.

If you're working in a more regimented prompt development cycle, you could credibly end up with something like this:

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

## Prompt to output links

There's a good reason why linking prompts to the outputs they generate is important:

You can access prompt performance by seeing what *results* you got from them!

If you're managing your LLM workspace using flat files (say, Obsidian, VS Code) a common convention is to use `YAML` frontmatter to note parameter elements, including backlinks.

## Prompt Snippets

In addition to full prompts, you can also consider adding prompts snippets.