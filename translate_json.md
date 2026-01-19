---
key: translate_json
name: Translate JSON
version: "1.0"
description: Translates JSON schema field strings while preserving exact structure
task_type: translation
required_variables:
  - target_language
optional_variables: []
tags:
  - translation
  - json
  - data
default_variables:
  target_language: English
default_model: gpt-4o-mini
output_mode: json
safety_level: safe
schema_version: "1.0"
---

## Task

Translate the given json schema into {{ target_language }}.

Maintain the exact structure of the schema.

Only translate the given field strings that are enclosed in double quotes ("").

Do not translate filenames or other referent objects whose names should remain consistent.

## Output

Do not add or omit any content.

Do not wrap the output in any way, such as with backticks ` or json or other formatting markers.

Just give the raw json schema in exactly the same format.
