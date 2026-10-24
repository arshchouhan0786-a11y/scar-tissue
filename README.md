# Scar Tissue

Memory recalls. Scars block.

Every AI agent repeats mistakes its user already corrected. The correction lives in a memory file, a transcript, a summary. Nothing checks it before the next action. So the agent does the same wrong thing again, and the user says "I told you already."

Scar Tissue fixes that one gap. A user correction becomes a scar: a hard pre-action gate, not a note. Before any consequential action, the agent scans its scars. Match means stop.

## How it works

1. **Record.** When the user corrects you, write a scar before the next action. One correction, one scar. Trigger concrete. Source quote verbatim.
2. **Check.** Before sending, posting, publishing, deleting, booking, paying, scheduling, sharing, or signing in, name the action and scan scars in scope. Global scars always apply.
3. **Stop.** Match means stop. No rephrasing around it. Name the scar that blocked it, offer the nearest allowed alternative.
4. **Review.** Every block increments a hit count. Monthly, surface the ledger. Only the user retires a scar.

## What counts as a scar

A correction of agent behavior that was wrong: a reversal, a ban, a corrected method, a corrected assumption.

Not a scar: a fact, a preference, a one-off instruction, a task decision. Those live in memory. Scars cover only behavior that must not repeat.

## Install

Copy `skills/scar-tissue` into your agent's skills directory. That is the whole install. No server, no key, no dependency.

Keep your ledger out of the repo. The ledger holds your corrections. It lives in your own files, not in public.

## Layout

- `skills/scar-tissue/SKILL.md` — the skill.
- `examples/SCARS.md` — fictional example ledger. Shows the format. Not real scars.

## License

MIT.
