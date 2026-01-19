---
key: generate_sections_en
name: Generate Sections English
version: "1.0"
description: Divides English text into logical sections with titles, summaries, and line numbers
task_type: sectioning
required_variables:
  - section_count
optional_variables: []
tags:
  - sectioning
  - english
  - analysis
default_model: gpt-4o
output_mode: json
safety_level: safe
schema_version: "1.0"
---

## Task

Divide the entire text into {{ section_count }} logical sections based on content. For each section, provide the title, summary, and starting/ending line numbers. Also provide a summary of the whole text.

## Input

Each line of the text is numbered in the format: `<NUM:LINE>`

## Output
Your output is a json response object. You must match the response object schema exactly.

IMPORTANT: 
- Every line in the text must belong to a section. 

- Don't leave out any lines. 

- Don't include lines in more than one section.
