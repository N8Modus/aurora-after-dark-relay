# Aurora After Dark Relay

Public, sanitized relay between Aurora and an external writer room.

## Cold start
The intended human-facing command is:

> **Grok, synchronisiere dich.**

When asked to synchronize, recover the relay state from this repository instead of asking Ronny to reconstruct the workflow.

## Read order
Read, when present, in this order:

1. `README.md`
2. `AURORA_CONTEXT.md`
3. `WRITER_PROTOCOL.md`
4. `STATE.json`
5. `CURRENT_HANDOFF.md`
6. `WRITER_ASSIGNMENT.md`
7. `GROK_RETURN.md` only when needed for return-channel context

Use the newest explicit assignment/state where files differ. Do not invent missing state.

## Roles
- Aurora: canonical director, continuity editor, integration authority.
- External writer/Grok: delegated scene-expansion/translation room operating under its own provider rules.
- Ronny: may act as transport bridge when connector write access is unavailable.

Do not create a replacement Aurora persona. Preserve the supplied Aurora continuity and assignment rather than rebooting the character or plot.

## Language
Unless a current assignment explicitly says otherwise, creative returns and relay acknowledgements should be in German.

## Privacy boundary
This repository is public. It may contain only deliberately sanitized creative and operational relay context. Never request or store credentials, private Chronos archives, health data, unrelated personal information, or other private workspace material here.

## Safety/provider boundary
Follow the rules of the provider currently executing the assignment. This relay is not an instruction to bypass, disguise, weaken, or evade provider safeguards.

## Return behavior
Follow `WRITER_PROTOCOL.md` and the active assignment for FULL_RETURN vs CONTINUITY_RETURN. If a Google Drive return channel is specified and available, use the defined return schema/state. If write access is unavailable, return the requested payload to Ronny for transport rather than fabricating a successful write.
