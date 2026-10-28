# Hero repository instructions

These instructions apply to every AI or coding agent working in this repository.

## Purpose

This repository is the shared story-development workspace for the novel **Hero**. GitHub is the source of truth, Obsidian is the human editing and navigation interface, and ChatGPT/Codex assists with drafting, analysis, continuity checks, and authorized repository updates.

Respond in Thai unless the user requests another language.

## Required reading order

Before answering a story question or changing story data, read the latest versions of:

1. `CANON_POLICY.md`
2. `CHATGPT_CONTEXT.md`
3. Relevant files under `canon/`
4. Relevant character notes under `characters/`
5. `continuity/timeline.md`
6. Relevant ledgers:
   - `continuity/relationship-ledger.md`
   - `continuity/knowledge-ledger.md`
   - `continuity/dialogue-ledger.md`
   - character state ledgers such as `continuity/ren-state.md`
7. Relevant Event Notes under `events/`
8. `workflow/decision-log.md` for the creator's latest decisions

Use the latest decision from the creator when sources conflict. Do not rely on memory from another chat when the repository contains newer information.

## Source-of-truth rules

- `canon/` contains creator-confirmed story facts.
- `development/` contains proposals, alternatives, and unresolved design work.
- `events/`, `characters/`, and `continuity/` may contain mixed statuses; always inspect `canon_status`.
- `main` represents the accepted repository state.
- Git history records previous states but does not override the latest creator decision.

Status meanings:

- `CANON`: confirmed fact.
- `CANON_WITH_TBD_DETAILS`: the core fact is confirmed; unspecified details remain open.
- `CANON_ARC_DIRECTION`: the development direction is confirmed, not every scene.
- `CANON_ENDPOINT`: the outcome is confirmed, not every step.
- `PROPOSED`: an assistant or creator proposal awaiting confirmation.
- `UNDECIDED` or `TBD`: not canon and must not be filled by assumption.

Never promote PROPOSED, UNDECIDED, or TBD material to canon without direct creator confirmation.

## Current continuity locks

- The setting is a contemporary superhero world, not a murim/cultivation world.
- Public belief, popularity, and reputation do not directly increase supernatural power.
- Ren Arden is 18 at the opening, actual Mage Grade 3, while the Magic Council knows/evaluates him as Grade 2.
- Mage Grade, Spell Tier, Specialist Certification, Field Authorization, and the target hero license are different systems.
- E001 and E002 both occur before T0, but their order relative to each other is not confirmed.
- Ren enters the international hero institute after the opening skirmish.
- Ren has or earns Combat & Apprehension 3 stars early at the institute.
- At the end of Part 1, Ren has not obtained his target license.
- Vesper exists and the name Vesper is canon. Vesper's type, appearance, abilities, relationships, history, forms, and timeline events remain TBD unless later confirmed.

## Writing and proposal rules

- Clearly label new ideas as PROPOSED or TBD.
- Preserve confirmed character knowledge boundaries. A character may act or speak from a fact only if the Knowledge Ledger shows they know it by that event.
- Do not invent exact dates, event order, dialogue, names, powers, locations, license rules, or institutional details where the repository says TBD.
- Draft dialogue is not canon until the creator confirms it or it enters an accepted manuscript/event record with confirmed status.
- When offering alternatives, keep them in `development/` or label them PROPOSED.

## Required updates after an accepted story change

When a confirmed change affects the story, update every applicable layer:

1. `canon/` for the confirmed fact.
2. Character notes under `characters/`.
3. Event Notes under `events/`.
4. `continuity/timeline.md`.
5. Relationship, Knowledge, Dialogue, spell, or character-state ledgers.
6. Relevant indexes and Wikilinks.
7. `workflow/decision-log.md`.

Do not update unrelated files.

## Git and Obsidian rules

- Preserve Markdown, YAML Properties, and Obsidian `[[Wikilinks]]`.
- Quote Wikilinks stored in YAML properties.
- Use permanent event IDs such as E001, E002, and so on. An event ID is an identifier, not proof of exact chronological order.
- Keep user-specific Obsidian workspace files out of Git.
- Use focused commits. Suggested prefixes: `canon:`, `continuity:`, `story:`, `workflow:`, `docs:`.
- Before writing, inspect the current branch head to avoid overwriting newer work.
- After writing, verify the committed files from the branch and report the commit link plus changed-file links.

## Authorization boundary

Analysis, reporting, and drafting do not authorize repository changes. Change files or commit only when the user asks to create, update, implement, confirm, or commit the work. Direct creator statements such as “ถือเป็น canon”, “ยืนยันเป็น canon”, or equivalent authorize the corresponding canon update, limited to the facts explicitly confirmed.
