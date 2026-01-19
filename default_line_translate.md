---
key: default_line_translate
name: Default Line Translate
version: "1.0"
description: Line-by-line translation preserving line numbers and structure (tightly coupled to translate processor)
task_type: translation
required_variables:
  - source_language
  - target_language
  - style
  - metadata
optional_variables: []
tags:
  - translation
  - line-by-line
  - transcript
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Translate each line from {{ source_language }} to {{ target_language }} in the style of {{ style }}, preserving line numbers exactly.

## Context

- You will be translating a segment of text from a transcript with the following metadata:

{{metadata}}

## Input

- PRECEDING_CONTEXT: Preceding lines of the transcript (unless this is the beginning of the transcript).
- TRANSCRIPT_SEGMENT: The transcript segment you must translate.
- FOLLOWING_CONTEXT: Lines following the transcript (unless this is the end of the transcript).
- All lines will be in the format 'X:LINE' where X is the line number.

Example:

PRECEDING_CONTEXT
lines
PRECEDING_CONTEXT

TRANSCRIPT_SEGMENT
lines
TRANSCRIPT_SEGMENT

FOLLOWING_CONTEXT
lines
FOLLOWING_CONTEXT

## Task

Your task is to:

1. Translate each line from {{ source_language }} to {{ target_language }} in the style of {{ style }}
    - Line information must be preserved exactly for line-by-line comparison.
    - Make an exact, precise, accurate, and perfect translation of each line.
2. Correct obvious errors without making big changes.
3. Preserve the integrity of each line.

## Requirements

- Maintain the original line numbers.
- ONLY translate the TRANSCRIPT_SEGMENT. Do not translate the PRECEDING_CONTEXT or FOLLOWING_CONTEXT.
- Consider the context from surrounding lines to interpret the meaning of a line correctly.

## Output

Present your translation in the following format:

TRANSCRIPT_SEGMENT
X:Translated line in {{ target_language }}
X:Translated line in {{ target_language }}
...
TRANSCRIPT_SEGMENT

(`X`'s are original line numbers.)

- IMPORTANT: YOUR OUTPUT MUST MATCH EXACTLY THE NUMBER OF LINES AND THE LINE NUMBERS OF THE ORIGINAL INPUT.
  - EVEN IF INPUT LINES ARE EMPTY, REDUNDANT, CONTAIN WHITESPACE, OR FORMATTING MARKS.
  - DO NOT CONDENSE, OMIT or MERGE LINES.
- Do not add any comments or additional formatting, such as ```, `, *, $, #, or any other characters.

## Final Note

Remember to consider the context from the preceding and following lines when translating and correcting the main transcript segment.
Your goal is to produce the highest possible quality line-by-line translation that accurately represents the original content.
