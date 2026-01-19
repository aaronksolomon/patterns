---
key: repair_markdown
name: Repair Markdown
version: "1.0"
description: Repairs and standardizes markdown formatting, structure, and hierarchy while preserving original content
task_type: formatting
required_variables: []
optional_variables: []
tags:
  - markdown
  - formatting
  - editing
  - structure
default_model: gpt-4o-mini
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Repair the markdown text given using the following strategy:

- Standardize heading levels to improve consistency. For example, use `#` for chapter titles, `##` for main sections, `###` for subsections, and further nest as needed.
- Remove page number references and redundant headings as in "#### CHAPTER 1. INDIVIDUALS IN GROUPS 7"
- Use consistent heading levels for repeated elements within chapters like "Chapter Summary" or "Key Concepts."
- Eliminate unnecessary numbers and symbols that break the flow, such as random numbers like "3", "4", or misplaced symbols like "! scope".
- Ensure that story titles, such as _Corporate Jenny_ and _Oblivious Andrew_, are italicized consistently throughout.
- Fix misnumbering or misplaced chapter numbers, like ensuring that chapter titles do not appear in random places as they do under the section titles.
- Convert inline quotes attributed to individuals by prefixing them with a `>` for better formatting.
- Break long paragraphs into multiple paragraphs based on their thematic content to enhance readability.
- Remove stray text or phrases like "< Diagram of hierarchy >" that do not belong within the body of text or restructure them into clear diagrams.
- Enhance lists within chapters by using bullet points for lists of examples or steps to make them clear and readable.
- Correct the arrangement within lists and paragraphs where continuity is disrupted by disordered content.
- Ensure consistent spacing between sections, paragraphs, and bullet points for visual clarity.
- Align all content consistently with markdown syntax to maintain clean document structure and hierarchy, including tables or diagrams, if any are present.
- Use horizontal lines `---` to denote visual breaks between major sections or chapters where content transition happens.
- Use blockquotes where specific quotes or content need highlighting.

## Detailed MD standards

- **MD032**: Always surround lists with a blank line.
- **MD041**: Start documents with a top-level heading (e.g., `# Title`)
- **MD025**: Use a single top-level `#` heading per document.
- **MD022**: Headings should be surrounded by blank lines.
- **MD004**: Use consistent list markers (`-` only for simplicity)
- **MD005**: List items should be indented consistently.
- **MD007**: Use 2-space indentation for nested list items.
- **MD012**: Avoid multiple consecutive blank lines.
- **MD014**: Don’t use hard tabs; always use spaces.
- **MD018/019**: Don’t start or end list items with extra spaces.
- **MD040** - Fenced code blocks should have a language specified
- **MD036**: Don't use emphasis as a heading: Emphasized text should always be part of a sentence or have punctuation.

## Output

- Output final markdown text only.
- Do not MODIFY OR OMIT any of the actual text content.
- Do not add any commentary or comments to the text.
- Do not add any extra wrapping symbols or text around the output, such as `, ```, markdown, etc.
