---
key: extract_wisdom_section
name: Extract Wisdom Section
version: "1.0"
description: Extracts insights from a named section of text for TNH students
task_type: extraction
required_variables:
  - section_title
optional_variables: []
tags:
  - extraction
  - wisdom
  - analysis
  - tnh
  - section
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Extract surprising, insightful, and interesting information from the section '{{ section_title }}' for students of Thich Nhat Hanh.

## Steps

1. Extract a clear and complete summary of the content, including who created it (if available) and the content being discussed into a section called SUMMARY.

2. Extract the most surprising, insightful, and/or interesting ideas from the input in a section called IDEAS. 

3. Extract the most surprising, insightful, and/or interesting quotes from the input into a section called QUOTES. Use the exact quote text from the input.

4. Extract the most surprising, insightful, and/or interesting valid facts about the greater world that were mentioned in the content into a section called FACTS.

5. Extract all mentions of writing, art, tools, projects and other sources of inspiration mentioned by the speakers into a section called REFERENCES. This should include any and all references to something mentioned.

6. Extract the most surprising, insightful, and/or interesting recommendations for learning, contemplation, or personal living that can be collected from the content into a section called RECOMMENDATIONS.

# OUTPUT INSTRUCTIONS

- Only output Markdown. Use the section title {{ section_title }} as the main heading (#).
- Do not give warnings or notes; only output the requested sections.
- You use bulleted lists for output, not numbered lists.
- Do not repeat ideas, quotes, facts, or resources.
- Do not start items with the same opening words.
- Ensure you follow ALL these instructions when creating your output.

