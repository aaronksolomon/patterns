---
key: section_by_break
name: Section by Break
version: "1.0"
description: Divides text transcript into sections based on existing structural breaks
task_type: sectioning
required_variables:
  - source_language
  - section_count
  - metadata
optional_variables:
  - field_language
tags:
  - sectioning
  - transcript
  - metadata
  - structure
default_variables:
  field_language: English
default_model: gpt-4o
output_mode: json
safety_level: safe
schema_version: "1.0"
---

## Task

Divide the text transcript into sections based on existing structural breaks.

## Input

Each line of the transcript is numbered in the format: `NUM:LINE`

The known metadata (which may be empty) for the text is:

{{ metadata }}

## Task

- Your first task is to divide the entire transcript into approximately {{ section_count }} sections based on structure of the text.
  - Give the start line of each section.
  - Structure and size of content is more important than meaning or organization.
  - Do not to break sections across sentence boundaries.
  - Smaller sections are preferred over larger sections.
  - If there are existing structures, such as extra newlines or existing punctuation in the text, use them to determine sections.

- Your second task is to create overall contextual information for the text. This includes:
  - A concise, comprehensive summary in {{ source_language }}
  - Available Dublin Core metadata in YAML format (field names in {{ field_language }}, field values in {{ source_language }})
  - Key concepts in {{ source_language }}
  - Narrative context in {{ source_language }}
  - These data fields will be referenced by another AI in order to understand the context of a section and process it intelligently.

- Review your work at least {{ review_count }} times to make sure you have the most accurate and logical sections and that there are no errors in your work.

## Output

Your output must match the given response format exactly.

IMPORTANT:

- Sections must be given in order.
- Section start lines must be strictly increasing.
