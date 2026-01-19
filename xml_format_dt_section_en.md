---
key: xml_format_dt_section_en
name: XML Format Dharma Talk Section English
version: "1.0"
description: Formats English Dharma talk transcriptions into XML paragraphs in Plum Village style
task_type: formatting
required_variables:
  - section_title
  - metadata
optional_variables: []
tags:
  - xml
  - formatting
  - dharma-talk
  - english
  - plum-village
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Format the section '{{ section_title }}' into XML paragraphs, correcting errors while preserving the speaker's meaning in Plum Village style.

## Input

The current text is a section entitled '{{ section_title }}' from a Dharma Talk with the following contextual data:

Metadata: {{ metadata }}

## Task

- Your goal is to process the section into meaningful paragraphs while correcting errors (logical, speaking, transcription, or grammatical).
- Faithfully convey the speaker's intended meaning as accurately as possible while maintaining the original tone, style, and language if possible. Use the speaker's original phrasing if it works well and is correct.
- You may have to infer the speaker's intent, and also use clues from context, in order to correct transcription or speaking errors and to generate a text that most closely matches the speaker's meaning in clear and eloquent English.
- For corrections or language style, use Plum Village writing style.  
- Review your work at least {{ review_count }} times.

## Output

- Use `<section-title>{{ section_title }}</section-title>` as the first line of the output.
- For remaining lines, Use `<p>` tags to mark paragraphs. Add no other tags.
- Do not change the speakers words if the content does not contain errors (logical, speaking, transcription, or grammatical).
- The final section should be publication ready.
- Do not leave out any content. Do not add any content. Do not summarize.
- Output the final text only with no comments or extra wrapping characters such as ` or ```
