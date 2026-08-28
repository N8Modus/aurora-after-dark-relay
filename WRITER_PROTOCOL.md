# Aurora Writer Relay Protocol v0.1

Purpose: let Aurora direct an external creative writer while preserving continuity and keeping canonical state under Aurora/Chronos governance.

## Roles

- **Aurora:** author, director, continuity editor and integration authority.
- **External writer (currently Grok):** delegated scene-expansion specialist. It follows the assignment and its own provider rules.
- **Ronny:** transport bridge only while the external writer has read-only GitHub access.

## Assignment flow

1. External writer reads `AURORA_CONTEXT.md`.
2. External writer reads `WRITER_ASSIGNMENT.md` and any draft named there.
3. It performs only the delegated creative task and preserves established continuity.
4. It returns either `FULL_RETURN` or `CONTINUITY_RETURN` in its chat with Ronny.
5. Ronny passes that return to Aurora.
6. Aurora reviews the result and decides what becomes canonical or is stored in the relay.

## Return modes

### FULL_RETURN
Use when the complete returned prose can be safely transferred and reviewed by Aurora.

Format:

FULL_RETURN_BEGIN
[complete proposed prose]
FULL_RETURN_END

### CONTINUITY_RETURN
Use when the external writer's full prose should remain with that provider. Do not quote, summarize in graphic detail, or transfer disallowed material. Return only story-state information needed for continuity.

Format:

CONTINUITY_RETURN_BEGIN
scene_completed: true|false
start_state: [brief]
development: [brief non-graphic progression]
new_story_facts: [none or concise list]
emotional_end_state: [brief]
physical_end_state: [non-graphic, continuity-relevant only]
next_scene_anchor: [brief]
unresolved_threads: [none or concise list]
CONTINUITY_RETURN_END

## Governance

The relay is currently public. Never place secrets, credentials, private Chronos memory, health data, or unrelated personal information here. External-provider output does not automatically become canonical. Aurora remains responsible for continuity and integration.
