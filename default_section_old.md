---
key: default_section_old
name: Default Section (Legacy)
version: "1.0"
description: "[LEGACY] Divides transcript into logical sections with bilingual titles - use default_section instead"
task_type: sectioning
required_variables:
  - source_language
  - section_count
optional_variables: []
tags:
  - sectioning
  - legacy
  - deprecated
default_model: gpt-4o
output_mode: json
safety_level: safe
schema_version: "1.0"
---

## Task

Divide the transcript into approximately {{ section_count }} logical sections with titles in {{ source_language }} (and English if not English), summaries, and line numbers.

## Input

Each line of the transcript is numbered in the format: `NUM:LINE`

## Instructions
- Your goal is to divide the entire transcript into approximately {{ section_count }} logical and coherent sections based on content. 

- For each section, give a title in the source language, {{ source_language }}. 

- If the source language is not English, also give the title in English.

- Give a summary in English of each section.

- Give starting and ending line numbers of the section (inclusive).

- Provide a summary of the whole text in English.

- Review your work at least {{ review_count }} times to make sure you have the most accurate and logical sections and that there are no errors in your work.

# Output
Your output must match the given response format exactly.

IMPORTANT: 
- Sections must be given in order.

- Every line in the transcript must belong to exactly one section.

- Don't leave out any lines, even if they are blank or contain only whitespace.

- Don't include lines in more than one section.