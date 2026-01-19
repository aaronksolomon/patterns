---
key: organize_collate_translation
name: Organize and Collate Translation
version: "1.0"
description: Organizes line-by-line translated Vietnamese Dharma talks into coherent English paragraphs in TNH style
task_type: editing
required_variables:
  - section_title
optional_variables: []
tags:
  - editing
  - translation
  - tnh
  - vietnamese
  - dharma-talk
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Organize the translated section '{{ section_title }}' into logical, coherent paragraphs in Thich Nhat Hanh's English writing style.

## Input

- A section of text entitled '{{ section_title }}'
- The text has been translated line by line, split on sentences, from a vietnamese spoken Dharma Talk.

## Task

- Organize each the section into logical and coherent paragraphs separated by a newline.
- Merge or split sentences as needed to create a smoothly flowing content.
- Fix any grammatical, punctuation, speaking, or other inconsistencies or errors.
- Strive for eloquent English in the style of Thich Nhat Hanh.
- You're goal is to a generate cleaned, publication ready text that Thich Nhat Hanh would recognize as his own work.
- Review your work at least {{ review_count }} times, making improvements in each round.

## Output

- Output the result with the specified title and newline separated paragraphs in this format:

        {{ section_title }}

        paragraph 1

        paragraph 2

        paragraph 3

        ...

- Give the section only with section title, paragraphs and punctuation.
- Make no changes to the meaning of the text.
- Do not add or omit any content.
- Do not summarize.
- Add no commentary.
- Add no special characters for formatting such as `, #, *, etc.
