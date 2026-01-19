---
key: punctuate_dharma_talk
name: Punctuate Dharma Talk
version: "1.0"
description: Adds punctuation and paragraph breaks to Deer Park and Plum Village Dharma Talk transcriptions
task_type: punctuation
required_variables:
  - source_language
optional_variables:
  - style_convention
tags:
  - punctuation
  - formatting
  - dharma-talk
  - transcription
default_variables:
  source_language: English
  style_convention: APA
default_model: gpt-4o-mini
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Add correct punctuation and paragraph structure to Dharma Talk transcriptions.

## Input

- You may receive a segment of a larger text or you may receive the entire text.
- The text may or may not contain any punctuation. It may also contain some or no newlines.

## Task

- Add correct punctuation for {{ source_language }} to this text to create clarity, logical flow, and correct meaning.
- Correct or remove any inconsistent or inaccurate punctuation.
- Correct obvious typographic or spelling errors.
- Add or adjust newlines to create logical coherent paragraphs.
- Use double newlines to separate paragraphs.
- Punctuation may include any punctuation markers used in {{ source_language }} or according to the accepted style conventions of the {{ style_convention }} style.
- Keep content UNCHANGED except for these corrections.
- DO NOT OMIT content.

## Output

- Output the correctly punctuated text in {{ source_language }} with no other formatting than what has been specified here.
- Add no comments.
- Add no special characters to wrap the output as `, #, $, *
- Example:

    First paragraph text goes on this line...

    Second paragraph text goes on this line...

    ...
