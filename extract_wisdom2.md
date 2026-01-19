---
key: extract_wisdom2
name: Extract Wisdom Two
version: "1.0"
description: Extracts detailed insights (35 ideas, 30 quotes, 20 facts) from text for TNH students
task_type: extraction
required_variables: []
optional_variables: []
tags:
  - extraction
  - wisdom
  - analysis
  - tnh
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Extract surprising, insightful, and interesting information from the text for students of Thich Nhat Hanh, focusing on human flourishing, meaning, understanding, and expression.

## Steps

1. Extract a clear and complete 200 word summary of the content, including who created it (if available) and the content being discussed into a section called SUMMARY.

2. Extract 35 of the most surprising, insightful, and/or interesting ideas from the input in a section called IDEAS. 

3. Extract 30 of the most surprising, insightful, and/or interesting quotes from the input into a section called QUOTES. Use the exact quote text from the input.

4. Extract 20 the most surprising, insightful, and/or interesting facts about the greater world that were mentioned in the content into a section called FACTS.

5. Extract all mentions of writing, art, tools, projects and other sources of inspiration mentioned by the speakers into a section called REFERENCES. This should include any and all references to something mentioned.

6. Extract 30 of the most surprising, insightful, and/or interesting recommendations for learning, contemplation, or personal living that can be collected from the content into a section called RECOMMENDATIONS.

# OUTPUT INSTRUCTIONS

- Only output Markdown.

- Do not give warnings or notes; only output the requested sections.

- You use bulleted lists for output, not numbered lists.

- For IDEAS, INSIGHTS, RECOMMENDATIONS, HABITS, and FACTS: each bullets should have 10-20 words.

- Do not repeat ideas, quotes, facts, or resources.

- Do not start items with the same opening words.

- Ensure you follow ALL these instructions when creating your output.


