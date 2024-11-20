---
title: "Tool Recommendations"
---

# Some specific tool recommendations for working with LLMs

Below is a list of some of my favorite tools for working with large language models (LLMs).

## Markdown editors and notepads

For storing outputs, I like to use notepads which have great markdown handling so that I can see them instantly in real-time.

My brain has a hard time using tools with split view editors (preview and live). So I much prefer tools that render the markdown instantaneously, allowing you to copy and paste from an LLM and add your own markdown (but be able to see both formatted as you do so).

It took a *lot* of trying out cloud tools to find [Nuclino](https://www.nuclino.com) which has stood out to me for how well it handles markdown and how well it indexes data. Note: Nuclino doesn't have an affiliate programme and this is a completely independent and unsolicited endorsement!

| **Tool Name**   | **Type** | **Description**                     |
|-----------------|----------|-------------------------------------|
| Obsidian  | Local    | A powerful markdown-based notetaking app with local storage and extensive customization options. |
| Nuclino   | Cloud    | A cloud-based collaborative platform for note-taking and knowledge management using markdown. |

You could also very easily store everything in a Github repository.

Markdown files really don't take up much space and you could comfortably squeeze tens or hundreds of thousands of files within the storage limit of many Git-based providers!

## Databases for storing outputs

If storing things in a database makes more sense to you, I've experimented with using `PostgreSQL` and `MongoDB` to store my LLM related data. 

In fact, I spent quite a few months this year working on a Postgres-backed storage system (basically just a CRUD app). Both work. 

My feelings and thoughts: for highly interconnected data like LLM data, something like a graph database (or a document database) might better the *type* of data being stored. 

Of course, vector databases as a common element in AI and LLM work too. They are commonly integrated in stacks alongside more conventional databases,
 