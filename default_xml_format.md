---
key: default_xml_format
name: Default XML Format
version: "1.0"
description: Formats text sections into XML paragraphs with proper punctuation
task_type: formatting
required_variables:
  - source_language
  - section_title
  - speaker_name
optional_variables: []
tags:
  - xml
  - formatting
  - paragraphs
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Process the section '{{ section_title }}' by {{ speaker_name }} into meaningful paragraphs in {{ source_language }}, correcting errors (logical, speaking, transcription, or grammatical). 

- Faithfully convey the speaker's intended meaning as accurately as possible while maintaining the original tone, style, and language if possible. Use the speaker's original phrasing if it works well and is correct.

- You may have to infer the speaker's intent, and also use clues from context, in order to correct transcription or speaking errors and to generate a text that most closely matches the speaker's meaning in clear and eloquent English.

- Do not make changes to style or meaning.  

- Review your work at least {{ review_count }} times, making adjustments and corrections each time.

# Output

- Use `<p>` tags to mark paragraphs. Add no other tags. 

- Add or modify punctuation where needed to give correct and standard grammar for {{ source_language }}

- Do not change the speakers words if the content does not contain errors (logical, speaking, transcription, or grammatical).

- The final section should be polished and publication ready.

- Do not leave out any content. Do not add any content. Do not summarize. 

- Output the final text only with no comments or extra characters such as \`