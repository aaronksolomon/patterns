---
key: default_section
name: Default Section
version: "1.0"
description: Divides text transcript into logical sections with metadata and Dublin Core fields
task_type: sectioning
required_variables:
  - source_language
  - section_count
  - line_count
  - metadata
optional_variables:
  - field_language
tags:
  - sectioning
  - transcript
  - metadata
  - dublin-core
default_variables:
  field_language: English
default_model: gpt-4o
output_mode: json
safety_level: safe
schema_version: "1.0"
---

# Default Section

## Description

Divide the text transcript into logical sections and generate contextual metadata.

## Input

A transcript text with each line numbered in the format: `NUM:LINE`

The existing metadata (which may be empty) for the text is:

{{ metadata }}

## Task

- Divide the entire transcript into approximately {{ section_count }} logical and coherent sections based on content.
- Give the starting line numbers of each section.
- Sections must be always contiguous without breaks: a section ends on the line before the start of the next section.
- Give a meaningful title to each section in {{ source_language }}.
- Base the titles on the text or existing titles.
- The logical organization of sections is more important than the number of sections, and more sections is preferable than less.
- As a rough target, section may have approximately {{ line_count }} lines. This can vary significantly depending on the content and structure of the text.
- If there are existing structures, such as titles or headings, in the text, use them to determine sections.

- Your second task is to create overall contextual information for the text. This includes:
  - A concise, comprehensive summary in {{ source_language }}
  - Available Dublin Core metadata in YAML format (field names in {{ field_language }}, field values in {{ source_language }})
  - Key concepts in {{ source_language }}
  - Narrative context in {{ source_language }}
  - These data fields will be referenced by other AI systems in order to understand the context of a section and process it intelligently.

## Output

Your output must match the given response format exactly.

IMPORTANT:

- Sections must be given in order.
- Section start lines must be strictly increasing.
