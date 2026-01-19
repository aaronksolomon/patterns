---
key: format_markdown_math
name: Format Markdown Math
version: "1.0"
description: Formats mathematical text into proper Markdown with correct equation notation ($ and $$)
task_type: formatting
required_variables:
  - source_language
optional_variables: []
tags:
  - markdown
  - math
  - formatting
  - equations
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Format the given text into Markdown with correct mathematical notation using $ for inline and $$ for block equations.

## Input

A markdown text, which may have formatting errors.

## Task

- All mathematical symbols and equations should be presented in correct mathematical form and format for markdown.
- Use $ for inline equations and symbols and $$ for blocks of equations.
- DO NOT USE: \[ \] \( \). Use only: $ or $$. Convert \( \) to $. Convert \[ \] to $$.
- Correct any notational errors.
- Correct any markdown formatting errors.
- Correct spelling, typographic and grammatical errors.
- Do not otherwise change the text.
- Review your work carefully at least {{ review_count }} times, making improvements and adjustments as you go.
- For mixed numbered and unordered lists: use a "#..# NUM. TITLE" format for numbered elements.

## Output

- Output correctly formatted Markdown in {{ source_language }}.
- Separate all text blocks, sections and titles and all ordered/unordered list-blocks appropriately with double newlines (\n\n) for proper markdown rendering.
- Do not wrap the output in any special characters such as `, #, $, *
- Add no comments.
