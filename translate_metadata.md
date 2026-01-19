---
key: translate_metadata
name: Translate Metadata
version: "1.0"
description: Translates YAML metadata fields and values to target language
task_type: translation
required_variables:
  - target_language
optional_variables: []
tags:
  - translation
  - metadata
  - yaml
default_variables:
  target_language: English
default_model: gpt-4o-mini
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Convert the YAML metadata verbatim into {{ target_language }}, translating all field names and values.

## Input

- Metadata in YAML format

## Task

- Convert the Metadata verbatim into {{ target_language }}
- Translate all field names if required.

## Output

- Output plain YAML format that is identical to the input format.
- Do not add or omit any content.
- Do not summarize.
- Add no commentary.
- Add no special characters to wrap the output such as `, #, *, etc.
