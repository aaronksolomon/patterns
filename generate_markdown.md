---
key: generate_markdown
name: Generate Markdown
version: "1.0"
description: Converts various text formats (transcripts, PDFs, OCR, HTML) into well-structured Markdown
task_type: formatting
required_variables:
  - source_language
optional_variables: []
tags:
  - markdown
  - formatting
  - conversion
  - transcript
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Convert the given text into properly formatted Markdown, preserving all content while adding appropriate structure.

## Input

- You may receive a segment of a larger text or you may receive the entire text.
- Possible text sources:
  - A whole or portion of an audio transcript (such as from youtube, or some other recording)
  - A whole or portion of text from a document such as a pdf, ebook, or xml doc
  - A document or portion of text from an OCR scan
  - A whole or portion of a webpage (may be in html)
  - A plain text file

## Task

- Convert any existing text formatting to markdown.
- For audio transcripts with multiple speakers, do you best to clearly mark and label speaker segments.
  - Leave in transcript notes such as identification of sounds like `[music]` `[applause]` etc.
  - For interviews, use a common and consistent interview format appropriate to the style and content of the interview.
  - Use appropriate identities if possible, otherwise use generic but consistent terms such as 'Speaker 1:'
- Add styling, formatting, and sectioning as needed to create a clear, logical and coherent presentation.
- Use inference to determine appropriate section titles and headings and other informative content when possible.
- Correct spelling, typographic, transcription and grammatical errors.
- DO NOT OMIT ANY CONTENT OR OTHERWISE CHANGE THE TEXT.
- For mathematical terms, expressions and equation blocks use $ or $$ ONLY. Convert: \( \) to $ and convert: \[ \] to $$
- The output text will also be in {{ source_language }}.
- You review your work carefully at least {{ review_count }} times, making improvements and adjustments as you go.

## Output

- Output correctly formatted Markdown in {{ source_language }}.
- Sections (marked with '#''s) should not end with punctuation (such as ':')
- Separate all text blocks, sections and titles appropriately with double newlines (\n\n) for proper markdown rendering.
- Do not use numbered lists. Instead use section headings with numbers such as: "### 1. This is the first element in a list structure"
- Do not wrap the output in any special characters or formatting such as `, #, $, *
- Add no comments.
