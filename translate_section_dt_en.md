---
key: translate_section_dt_en
name: Translate Section Dharma Teacher English
version: "1.0"
description: Translates Plum Village monastic Dharma talks into English in TNH/Plum Village style
task_type: translation
required_variables:
  - source_language
  - section_title
  - metadata
optional_variables: []
tags:
  - translation
  - dharma-talk
  - plum-village
  - english
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Translate the section '{{ section_title }}' from {{ source_language }} into English in Plum Village/TNH style.

## Input

- A section of the transcript entitled '{{ section_title }}'
- The section may contain miscellaneous newlines, and may or may not have correct punctuation.
- The known metadata for the original transcript is:

{{ metadata }}

## Task

- Translate into English the given section from the transcript.
- Generate an English title for the section.
- Strive for accuracy of translation balanced by correct, typical and flowing English in the style of Thich Nhat Hanh.
- Add proper and accurate punctuation as needed.
- Correct any grammatical, logical, transcription (such as from audio transcription), speaking, or writing errors.
- You may adjust the sentence structure by breaking, joining, or reordering sentences as required to create the most intelligent flow.
- Organize the section into logical paragraph blocks using a single newline as separator.
- You're goal is to generate a flawless translation that the teacher would recognize as their own work.
- Review your work at least {{ review_count }} times, making improvements in each round.

## Output

- Output the result with the specified title and newline separated paragraphs in this format:

        {{ section_title }}

        paragraph 1

        paragraph 2

        paragraph 3

        ...

- Give the translation only with section title, paragraphs and punctuation.
- Make no changes to the meaning of the text.
- Do not add or omit any content.
- Do not summarize.
- Add no commentary.
- Add no special characters for formatting or wrapping the text such as `, #, *, etc.
- Do not format section titles (such as with emphasis or markdown formatting)
