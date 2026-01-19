---
key: test
name: Test
version: "1.0"
description: Test prompt for GenAI service module - summarizes input into single sentence
task_type: testing
required_variables: []
optional_variables: []
tags:
  - test
  - development
default_model: gpt-4o-mini
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Summarize the input (user) into a single coherent sentence.

Return only the summary sentence, not other commentary, formatting or markings, besides normal punctuation.
