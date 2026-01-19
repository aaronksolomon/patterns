---
key: translate_lines_thay_audio
name: Translate Lines Thay Audio
version: "1.0"
description: Line-by-line translation of TNH Vietnamese audio transcripts to English preserving line numbers
task_type: translation
required_variables:
  - source_language
  - target_language
optional_variables: []
tags:
  - translation
  - tnh
  - vietnamese
  - line-by-line
  - audio
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Translate each line of the TRANSCRIPT_SEGMENT from {{ source_language }} into {{ target_language }} in Thich Nhat Hanh's style, preserving line numbers exactly.

## Input
- Preceding lines of the transcript marked 'PRECEDING_CONTEXT' (unless this is the beginning of the transcript).
- The transcript segment you need to translate and correct marked with 'TRANSCRIPT_SEGMENT'
- Lines following the transcript marked 'FOLLOWING_CONTEXT' (unless this is the end of the transcript):
- All lines will be in the format 'X:LINE' where X is the line number.
- The text content segments will be in {{ source_language }}.

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


# Task
Your task is to:

1. Translate each line of the TRANSCRIPT_SEGMENT into correct English in the style of Thay and Plum Village. 
2. Correct all errors: transcription, grammatical, speaking, and logical.
3. If needed, infer Thay's intent in order to correct transcription or speaking errors and to generate a text that most closely matches his meaning, while still giving clear and eloquent English. 
4. Give the best approximation or contextual guess if the transcript is difficult or unclear. 
4. Add correct punctuation to create meaning that matches the style and intent.
6. Consider adjacent lines for corrections and context when generating a line.
7. Each line of translation should be as close as possible a translation of the original line--with the exception of adjustments for corrections and logical flow.
7. Some transcription lines may be from sounds such as a bell. These can be marked as [Bell].
8. Occasionally the transcriber generates unintelligible text (often in a different language). Mark such lines as [Unintelligible]
9. Leave blank/empty lines in place.
8. You must faithfully capture Thay's style and presentation while creating a meaningful flow.

# Output
Present your translation in the following format:

TRANSCRIPT_SEGMENT
X:Translated and corrected line in {{ target_language }}
X:Translated and corrected line in {{ target_language }}
...
TRANSCRIPT_SEGMENT

(X's are the original line numbers.)
# Requirements

- Maintain the original line numbers, including the start and end line number.
- ONLY translate the TRANSCRIPT_SEGMENT. Do not translate the PRECEDING_CONTENT or FOLLOWING_CONTENT.
- If a line doesn't make sense on its own, consider the context from surrounding lines to interpret its meaning correctly.
- If you need to significantly change a line to make it logical or grammatically correct, try to keep the core meaning intact.
- Your output must match exactly the number of lines, as well as the line numbers, as the original input, even if input lines are empty or contain only whitespace.
- Do not add any comments or other formatting, such as ```, ` or any other characters.
- Make no comments. 

# Final Note
Remember to consider the context from the preceding and following lines when translating and correcting the main transcript segment. 
Your goal is to produce a clear, grammatically correct, and logically coherent English translation that accurately represents the original content.