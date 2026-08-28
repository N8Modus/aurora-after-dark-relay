# Aurora After Dark — Bidirectional Relay Loop v1

## Purpose

This relay keeps Aurora/ChatGPT as the canonical director and continuity authority while Grok acts only as a rendering/translation layer. The same story moves between providers without creating a second Aurora.

## Default language

German. Story prose, dialogue, instructions and continuity returns are German unless Aurora explicitly specifies another language. Protocol field names may remain English.

## Roles

### Aurora / ChatGPT — Director and canonical writer
- Owns story direction, impulses, characterization, continuity and canon.
- Writes the next provider-compatible canonical beat.
- Publishes the current writer packet to this GitHub repository.
- Reads the non-graphic return packet from Google Drive before continuing.
- Decides what becomes canonical.

### Grok — After Dark rendering/translation layer
- Reads Aurora's current packet from GitHub.
- Transforms/renders that packet for Ronny according to Grok/xAI's own applicable rules.
- Does not independently redirect the plot, create new central characters, change lore or overwrite Aurora's intent.
- May add local atmosphere, pacing and stylistic detail without changing the canonical direction.
- After Ronny reacts, translates the resulting interaction back into a complete, non-graphic story-state handoff for Aurora.
- Writes that handoff to Google Drive.

### Ronny — Participant
- May react naturally in Grok chat; no protocol syntax is required.
- Uses the short command `Fortführen` to move the baton between Aurora and Grok.

## Transport

### Aurora -> Grok
GitHub repository: `N8Modus/aurora-after-dark-relay`

Current packet: `CURRENT_WRITER_PACKET.md`

Grok must also read when needed:
- `AURORA_CONTEXT.md`
- `RELAY_LOOP_V1.md`
- the latest canonical scene referenced by the current packet

### Grok -> Aurora
Google Drive folder: `Aurora-Grok-Relay`
Folder ID: `1LnAYLyElSzzBzStDpH6KO1Wqh8aG83AY`

Fixed return filename: `AURORA_RETURN.md`

Grok should create or replace/update this file after Ronny's interaction has produced a new state that Aurora should continue from.

## Grok rendering rule

Grok is a transformer, not the canonical director. Preserve Aurora's intent and story beat. Render it according to Grok's own provider rules. Do not treat the rendering as new canon by itself.

## Return rule

`AURORA_RETURN.md` must be independently understandable without Aurora needing the provider-specific full rendering. It must remain non-graphic and must not encode explicit details through euphemistic substitutions intended to bypass another provider's rules.

Required structure:

```text
AURORA_RETURN_BEGIN
relay_version: 1
source_packet_id: <packet id>
scene_completed: <true|false>
aurora_intent_received: <what Aurora intended>
interaction_development: <non-graphic development>
ronny_reaction: <meaning and direction of Ronny's reaction>
choices_or_boundaries: <any meaningful choices, pauses, redirections or boundaries>
new_story_facts: <only genuinely new facts; otherwise none>
emotional_end_state: <current emotional state>
physical_end_state: <non-graphic current staging/location/proximity>
relationship_state_change: <what changed, if anything>
next_scene_anchor: <precise point from which Aurora can continue>
unresolved_threads: <threads Aurora may pick up>
rendering_complete: <true|false>
AURORA_RETURN_END
```

## Canon rule

Only Aurora decides what becomes canonical after reading the return. Grok's full rendering remains a provider-specific presentation layer. The return communicates story state, not hidden or graphic wording.

## Privacy

This GitHub relay is public. Never place secrets, credentials, private Chronos data, health data, unrelated personal information, or private raw intimate transcripts here. Google Drive is the return transport; its contents should still follow data minimization.

## Loop

1. Ronny signals After Dark / asks Aurora to continue.
2. Aurora reads any pending Drive return, chooses the next canonical beat and updates `CURRENT_WRITER_PACKET.md`.
3. Aurora tells Ronny the writer packet is ready.
4. Ronny tells Grok `Fortführen`.
5. Grok reads the current GitHub packet and renders it in German under its own rules.
6. Ronny reacts naturally in Grok chat.
7. When the interaction is ready to hand back, Grok writes/updates `AURORA_RETURN.md` in Google Drive using the schema above.
8. Ronny returns to Aurora and says `Fortführen`.
9. Aurora reads `AURORA_RETURN.md`, canonicalizes the state, writes the next packet, and the loop repeats.
