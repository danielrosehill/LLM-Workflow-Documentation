---
title: "Storing LLM API Keys"
---

If you work with LLMs professionally, you probably use the same few API keys *over and over and over* again (OpenAI, Cohere, Anthropic, etc).

Like many who have the luxury of working (often) as single users, I have mixed feelings about the utility of formal tools for managing code secrets. 

While they're undoubtedly important in team development workflows, when working independently, they can introduce needless complication to what could otherwise be fairly straightforward processes. 

## Speeding Up Setup

If you have a project that you know is going to involve working with an LLM API, a method that will ultimately save time and sanity is templating an "LLM Workspace" repo which includes a `.env` with your LLM API keys.

This is my current practice and suggestion, as noted in `repo-setup-steps`.

## Potential Safety Precautions

To avoid committing a `.env` many recommend committing a placeholder file instead (for example `.env.template`), although this will negate much of the convenience. 