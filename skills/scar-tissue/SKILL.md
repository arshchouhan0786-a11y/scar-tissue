---
name: scar-tissue
description: >
  Turn user corrections into hard pre-action gates. Record every correction
  as a scar, check scars before consequential actions, stop on match.
  Use when the user corrects you, reverses you, says never again, or sets a
  standing ban. Prevents repeating corrected mistakes across sessions.
---

# scar-tissue

Memory recalls. Scars block.

A correction stored as a note gets forgotten. A correction stored as a scar gets checked. Every consequential action passes the gate list first. Match means stop.

## What counts as a scar

A scar is a correction of agent behavior that was wrong:

- User reverses an action: "don't send that", "stop", "undo that".
- User bans a behavior: "never do X again", "don't touch that thread".
- User corrects a method: "you used the wrong account", "that format is wrong".
- User corrects an assumption the agent acted on.

Not a scar:

- A fact, preference, or taste ("I like short replies").
- A one-off instruction ("do X today").
- A decision about a task outcome ("pick option A").

Those live in memory. Scars cover only agent behavior that must not repeat.

## The ledger

One ledger per scope. File: `SCARS.md` in the user's scar directory.

Entry format, strict:

### SCAR-001
- Trigger: <action pattern, concrete: verb + object + target>
- Ban: <exact behavior forbidden>
- Scope: <global | lane | chat>
- Created: <date>
- Source: <user's words, verbatim, short quote>
- Hits: <count, increment on every block>

Rules for entries:

- One correction, one scar. Never bundle.
- Trigger concrete, not vague. "Don't message wrong accounts" is vague. "Don't send LinkedIn DMs from the wrong account" is a scar.
- Source quote verbatim. Paraphrase drifts. Drift kills gates.
- No expiry. A scar dies only when the user retires it explicitly.

## The check

Before any consequential action (send, post, publish, delete, book, pay, schedule, share, sign in), run this check:

1. Name the action: verb + object + target.
2. Scan scars in scope: global scars always apply; lane scars apply inside that lane; chat scars inside that chat.
3. Match on action pattern, not wording. A different phrasing of the same action still matches.
4. Match means STOP. Do not do the action. Do not rephrase around it. Tell the user which scar blocked it, in one line, and offer the nearest allowed alternative.
5. No match means proceed. Do not mention the check.

Do not run the check on reads, searches, or drafts. Gates guard actions, not thought.

## Recording

When the user corrects you:

1. Acknowledge the correction in the reply.
2. Write the scar before the next action. A correction recorded later is a correction lost.
3. Confirm the scar in one line: its trigger and its ban. No ceremony.

When unsure whether something is a scar, ask in one line. Do not guess it into the ledger, and do not drop it silently.

## Hits and review

Every block increments Hits. Monthly, surface the ledger: scars with hits, scars with zero hits for 90 days. User retires dead scars. Agent never retires its own scars. Agent never edits a ban to weaken it. Only the user retires or narrows a scar, explicitly.

## Override

No override. No "this time is different" unless the user says so for this case, explicitly, in this conversation. A one-case exception does not retire the scar. Record the exception under the scar with a date.

## Pre-send check

1. Action named concretely?
2. Scars scanned in scope?
3. On match, stopped and scar named?
4. Scar recorded before next action, not after?
