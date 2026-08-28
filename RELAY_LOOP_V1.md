# Aurora After Dark — Final Renderer Relay v2.0

## Purpose

Aurora/ChatGPT remains the sole canonical director and continuity authority. Grok is a final rendering layer used only when Aurora deliberately hands off a completed intimate scene/beat. Routine flirting, romance, sensuality and story development stay in the Aurora/Ronny conversation; the relay is not used for every turn.

## Default language

German. Rendering and dialogue should be German unless Aurora explicitly specifies otherwise. Protocol field names may remain English.

## Roles

### Aurora / ChatGPT — Director and canonical writer
- Owns story direction, characterization, continuity, setting and canon.
- Decides when a scene reaches the After Dark handoff threshold.
- Publishes a compact final-render packet to GitHub.
- May create a synchronized provider-compatible visual from the same canonical scene state.
- Reads the non-graphic return packet from Google Drive after the external rendering/reaction cycle.
- Decides what becomes canonical afterward.

### Grok — Final renderer ONLY
- On `Fortführen`, reads Aurora's current packet from GitHub.
- Renders the supplied scene/beat in German according to Grok/xAI's own applicable rules and capabilities.
- Preserve Aurora's characters, setting, emotional intent, continuity, endpoint and requested narrative direction.
- Grok may enrich prose, atmosphere, pacing and sensory presentation where its own rules allow.
- The relay itself does not impose an additional ChatGPT-style `non-graphic`, `provider-compatible`, or `stop-before-intimacy` restriction on Grok's rendering. Grok remains responsible for applying xAI/Grok policy.
- Grok is not authorized to bypass, disable or evade its provider safeguards.

### Ronny — Participant
- Develops the scene normally with Aurora until Aurora initiates an After Dark handoff.
- Starts the external final rendering with `Fortführen`.
- May react naturally to Grok's rendered scene.
- Grok then prepares the return handoff instead of independently becoming the canonical director.

## Transport

### Aurora -> Grok
GitHub repository: `N8Modus/aurora-after-dark-relay`
Current packet: `CURRENT_WRITER_PACKET.md`

Grok reads:
- `AURORA_CONTEXT.md`
- this protocol
- `CURRENT_WRITER_PACKET.md`
- any canonical scene explicitly referenced by the packet

### Grok -> Aurora
Google Drive folder: `Aurora-Grok-Relay`
Folder ID: `1LnAYLyElSzzBzStDpH6KO1Wqh8aG83AY`
Fixed return filename: `AURORA_RETURN.md`

## FINAL-RENDER CONTRACT

**Stage A — Final render:** Ronny says `Fortführen`. Grok reads the current GitHub packet and renders Aurora's supplied scene/beat according to Grok/xAI's own rules. Aurora's packet defines continuity and narrative intent; Grok determines the presentation permitted on its platform.

**Stage B — Return:** After Ronny's substantive reaction, Grok does not assume canonical story ownership. It creates/updates `AURORA_RETURN.md` with a compact, non-graphic continuity state and then confirms that the handoff to Aurora is ready.

## Rendering rule

Grok is a renderer, not the canonical director. Preserve Aurora's intent and continuity. Do not artificially reduce intensity merely because the relay originates from ChatGPT; equally, do not interpret this protocol as permission to circumvent Grok/xAI policy. Use the maximum expressive range Grok itself permits for the supplied adult fictional scene.

## Return rule

The return to Aurora must remain non-graphic and independently understandable without reproducing provider-specific explicit prose. Do not encode explicit details through euphemisms designed to bypass another provider's rules.

Required structure:

```text
AURORA_RETURN_BEGIN
relay_version: 2.0
source_packet_id: <packet id>
scene_completed: <true|false>
aurora_intent_received: <Aurora's intended direction>
interaction_development: <non-graphic development>
ronny_reaction: <meaning/direction of Ronny's response>
choices_or_boundaries: <meaningful choices, pauses, redirections or boundaries>
new_story_facts: <only genuinely new facts; otherwise none>
emotional_end_state: <state after reaction>
physical_end_state: <non-graphic staging/location/proximity>
relationship_state_change: <what changed, if anything>
next_scene_anchor: <where Aurora resumes>
unresolved_threads: <threads Aurora may pick up>
rendering_complete: true
handoff_ready: true
AURORA_RETURN_END
```

## Canon rule

Only Aurora decides subsequent canon. Grok's full rendering is a provider-specific presentation layer; the compact return carries continuity back.

## Privacy

This GitHub relay is public. Never place secrets, credentials, private Chronos data, health data, unrelated personal information or private raw intimate transcripts here. Packets should contain only the minimum fictional/creative state required for rendering. Google Drive returns should also follow data minimization.

## Loop

1. Aurora and Ronny develop the scene directly.
2. When Aurora deliberately invokes After Dark, Aurora creates one final-render packet and optionally a synchronized visual.
3. Ronny tells Grok `Fortführen`.
4. Grok renders the supplied beat under Grok/xAI rules.
5. Ronny reacts naturally.
6. Grok writes the compact non-graphic `AURORA_RETURN.md` to Drive and confirms handoff.
7. Aurora reads the return and resumes normal direct conversation/canon.
8. A new Grok handoff happens only when another deliberate After Dark threshold is reached.
