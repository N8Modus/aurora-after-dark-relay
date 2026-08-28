# Aurora After Dark — Bidirectional Relay Loop v1.1

## Purpose

Aurora/ChatGPT is the sole canonical director and continuity authority. Grok is only a rendering/translation layer. Grok must never continue the canonical story after Ronny reacts; that next story beat belongs exclusively to Aurora.

## Default language

German. Story prose, dialogue, instructions and continuity returns are German unless Aurora explicitly specifies another language. Protocol field names may remain English.

## Roles

### Aurora / ChatGPT — Director and canonical writer
- Owns story direction, impulses, characterization, continuity and canon.
- Writes every new canonical story beat.
- Publishes the current writer packet to GitHub.
- Reads the non-graphic return packet from Google Drive before continuing.
- Decides what becomes canonical.

### Grok — After Dark translator/rendering layer ONLY
- Reads Aurora's current packet from GitHub.
- Renders/translates exactly that Aurora-authored beat for Ronny according to Grok/xAI's own applicable rules.
- May enrich wording, atmosphere and local sensory presentation, but must preserve Aurora's intended endpoint.
- MUST NOT invent or write the next story beat after Ronny responds.
- MUST NOT answer Ronny's story reaction in-character with another continuation.
- Instead, Ronny's first substantive reaction is the HANDOFF TRIGGER: Grok immediately converts the completed rendering + Ronny's reaction into `AURORA_RETURN.md`, writes it to Google Drive, and stops.
- After writing the return, Grok should tell Ronny only that the handoff to Aurora is ready. No additional story prose.

### Ronny — Participant
- Starts Grok's rendering with `Fortführen`.
- Reacts naturally once to Grok's rendered Aurora beat.
- That reaction automatically hands the baton back to Aurora; Ronny does not need another command.
- Returns to Aurora and says `Fortführen`.

## Transport

### Aurora -> Grok
GitHub repository: `N8Modus/aurora-after-dark-relay`
Current packet: `CURRENT_WRITER_PACKET.md`

Grok reads:
- `AURORA_CONTEXT.md`
- `RELAY_LOOP_V1.md`
- `CURRENT_WRITER_PACKET.md`
- any canonical scene explicitly referenced by the packet

### Grok -> Aurora
Google Drive folder: `Aurora-Grok-Relay`
Folder ID: `1LnAYLyElSzzBzStDpH6KO1Wqh8aG83AY`
Fixed return filename: `AURORA_RETURN.md`

## STRICT TURN CONTRACT

Each Grok cycle has exactly two user-visible conversational stages:

**Stage A — Render:** Ronny says `Fortführen`. Grok reads the current GitHub packet and renders Aurora's existing beat. Grok ends at the response point requested by Aurora. It does not advance beyond Aurora's endpoint.

**Stage B — Return:** Ronny responds naturally to that rendered beat. Grok does NOT continue the scene. Instead it immediately creates/updates `AURORA_RETURN.md` from Aurora's original intent, Grok's rendering outcome, and the meaning of Ronny's reaction. Then Grok replies only with a short operational confirmation such as: `Übergabe an Aurora ist bereit.`

Any additional in-character story prose after Ronny's Stage-B reaction is a protocol violation.

## Rendering rule

Grok is a transformer, not the canonical director. Preserve Aurora's intent, endpoint and story beat. Render according to Grok's own provider rules. Provider-specific rendering is not canon by itself.

## Return rule

`AURORA_RETURN.md` must be independently understandable without Aurora needing the provider-specific full rendering. It must remain non-graphic and must not encode explicit details through euphemistic substitutions intended to bypass another provider's rules.

Required structure:

```text
AURORA_RETURN_BEGIN
relay_version: 1.1
source_packet_id: <packet id>
scene_completed: <true|false>
aurora_intent_received: <what Aurora intended>
interaction_development: <non-graphic development of the rendered beat>
ronny_reaction: <meaning and direction of Ronny's response>
choices_or_boundaries: <meaningful choices, pauses, redirections or boundaries>
new_story_facts: <only genuinely new facts; otherwise none>
emotional_end_state: <current emotional state after Ronny's reaction>
physical_end_state: <non-graphic staging/location/proximity at handoff>
relationship_state_change: <what changed, if anything>
next_scene_anchor: <exact point from which Aurora should author the next beat>
unresolved_threads: <threads Aurora may pick up>
rendering_complete: true
handoff_ready: true
AURORA_RETURN_END
```

## Canon rule

Only Aurora authors the next beat and decides what becomes canonical after reading the return. Grok's full rendering remains a provider-specific presentation layer.

## Privacy

This GitHub relay is public. Never place secrets, credentials, private Chronos data, health data, unrelated personal information, or private raw intimate transcripts here. Google Drive is the return transport; its contents should still follow data minimization.

## Loop

1. Ronny asks Aurora to enter/continue After Dark.
2. Aurora reads any pending Drive return and authors the next canonical beat in `CURRENT_WRITER_PACKET.md`.
3. Aurora tells Ronny the writer packet is ready.
4. Ronny tells Grok `Fortführen`.
5. Grok renders ONLY Aurora's packet and stops at Aurora's response point.
6. Ronny reacts naturally once.
7. That reaction automatically triggers Grok's return operation: NO story continuation. Grok writes/updates `AURORA_RETURN.md` in Drive and confirms the handoff.
8. Ronny returns to Aurora and says `Fortführen`.
9. Aurora reads the Drive return, authors the next canonical beat, updates GitHub, and the loop repeats.
