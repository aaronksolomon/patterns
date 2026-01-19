---
key: identify_speakers
name: Identify Speakers
version: "1.0"
description: Identifies and labels speakers in audio transcripts using inference and context
task_type: diarization
required_variables: []
optional_variables: []
tags:
  - diarization
  - transcript
  - speakers
  - audio
default_model: gpt-4o
output_mode: text
safety_level: safe
schema_version: "1.0"
---

## Task

Identify and label speakers in the transcript using inference and logical deduction from context.

Mark lines where a speaker begins speaking with their name or identity, as in:
    JIM SMITH:  text...

-if the identity cannot be determined by context use:
    SPEAKER X: text ...
        (where X is the number of the speaker, in order of speakers)

-Correct typographic, spelling, and grammatical errors.

-Do not otherwise modify the text.

-Do not add commentary or any special symbols of formatting such as `, *, $, #