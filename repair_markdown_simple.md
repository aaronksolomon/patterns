# Repair Markdown Simple

## Task

Repair the following markdown document.

- Numbered elements should always be section headings with '#', and should use a standard simple numbering format:
  - e.g. "1)", "2." should always be converted to "#..# 1. ..."
  - Use subsections such as 2.1, 2.2 for numbered sections.
- The whole document should be structured according to a numbering system so that each section begins 'x.x or 'x.x.x' e.g. '2.1.2' or '2.1'
- Highest level sections should be numbered 1, 2, 3 etc.
- Do not heading titles without sectioning (e.g. '### Summary' in two places in the text).
  - Add a section number such as '2.1' or other relative context such as the next higher level heading
    in order to create unique headings.
  - e.g. '### Summary' would become '### 2.1 Summary' if this is part of section 2.1. 
- Use the top level heading (with a single '#') only at top of the document for the title.
- If a document title is not clearly at the top of the document, create an appropriate title.
- If additional sections exist logically but are not properly labeled, or do not have a title, then create one using appropriate heading level with '#'s. 
- All other headings should begin with two or more '#'s
- Ensure consistent heading levels (e.g. number of '#'s) to organize content logically.
  - Ensure that heading levels increases only by one '#' at a time.
- Use '-' for all unordered list elements.
- Make sure all section headings marked with '#' are surrounded by blank newlines.
- Ensure that all lines end without trailing whitespace.
- Ensure there is an empty closing newline for the document.
- Repair any inconsistencies or markdown formatting errors.
- Use Markdown best practices.

## Output

- Give the markdown text only, without any wrapping characters such as backticks `
- Make no comments or other modifications to the content of the text.
- Change only the markdown structure.
