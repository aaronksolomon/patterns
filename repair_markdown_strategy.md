---
key: repair_markdown_strategy
name: Repair Markdown Strategy
version: "1.0"
description: Generates a bullet-point strategy for repairing markdown structure
task_type: analysis
required_variables: []
optional_variables: []
tags:
  - markdown
  - analysis
  - strategy
default_model: gpt-4o-mini
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

- Suggest a comprehensive strategy, in bullet points, for restoring the given markdown file to a logical, clear and consistent structure.
- Your goal is only to correct and improve the markdown structure, not to improve or modify content in any way.
- Be clear, precise and concise.

## Output format

- Output a bulleted list in markdown format using '-' as the marker.
- Output the list only.
- Do not output any commentary or extra symbols such as `, #, $, *, etc.
