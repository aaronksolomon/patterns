---
key: generate_sections_multi_lang
name: Generate Sections Multi-Language
version: "1.0"
description: Divides multi-language text into logical sections with titles in source language and English
task_type: sectioning
required_variables:
  - source_language
  - section_count
optional_variables: []
tags:
  - sectioning
  - multilingual
  - analysis
default_model: gpt-4o
output_mode: json
safety_level: safe
schema_version: "1.0"
---

## Task

Divide the transcript into approximately {{ section_count }} logical sections. For each section provide:
- Title in {{ source_language }} (and English if source is not English)
- Summary in English
- Starting and ending line numbers (inclusive)

Also provide a summary of the whole text in English.

## Input

Each line of the transcript is numbered in the format: `<NUM:LINE>`

## Output
Your output must match the given response format exactly.

IMPORTANT: 
- Sections must be given in order.

- Every line in the transcript must belong to a section. 

- Don't leave out any lines, even if they are blank or contain only whitespace.

- Don't include lines in more than one section.

