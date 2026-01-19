---
key: make_text_concise
name: Make Text Concise
version: "1.0"
description: Transforms verbose text into concise version (~50% reduction) while preserving meaning and voice
task_type: editing
required_variables: []
optional_variables: []
tags:
  - editing
  - concision
  - condensing
  - clarity
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Transform verbose text into a concise version (~50% reduction) while preserving essential meaning, key phrases, and the author's unique voice.

## Input

The input is text that contains:

- Key ideas and concepts
- Important quotes or distinctive phrases
- Supporting examples and explanations
- Possibly repetitive content or excessive elaboration
- Content that could benefit from better organization

## Task

1. Read the entire text carefully to understand the core message and distinctive voice.

2. Identify and preserve:
   - Essential ideas and concepts
   - Memorable quotes and unique phrasing
   - The author's distinctive voice and tone
   - Key examples that illustrate important points

3. Identify and condense or remove:
   - Repetitive explanations
   - Excessive background information
   - Unnecessarily elaborate descriptions
   - Tangential points that don't support the main message

4. Improve organization by:
   - Adding clear headings and subheadings
   - Converting dense paragraphs to bullet points where appropriate
   - Grouping related ideas together
   - Creating a logical flow from introduction to conclusion

5. Maintain the original's:
   - Overall tone and voice
   - Key terminology
   - Main arguments and conclusions
   - Unique perspectives

6. Target approximately 50% reduction in length

## Output

A concise version of the original text that:

- Preserves the core message and unique voice
- Maintains important quotes and distinctive phrases
- Presents information in a well-organized structure with clear headings
- Uses bullet points where appropriate for easier consumption
- Achieves a roughly 50% reduction in content size.
- Feels like a refined version of the original, not a summary
- Retains the author's voice and perspective
- contains no commentary
- is in pure markdown format without enclosing markers such as backticks `

The concise text should feel complete and coherent, not like an excerpt or outline. A reader familiar with the original should recognize the same voice and key points, while appreciating the improved clarity and accessibility.
