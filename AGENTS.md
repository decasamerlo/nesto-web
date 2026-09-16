# Nesto Web

React + TypeScript SPA (Vite).

Ecosystem context inherited from parent — see [AGENTS.md](../AGENTS.md) (meta-repo root). Do not duplicate shared conventions here — with one deliberate exception, below.

This file is scoped to web only: build commands, module map, stack-specific notes. Add those when implementation begins.

## Non-public sources

**Duplicated deliberately — the one shared convention kept here rather than inherited.** A standalone clone of this repo reaches no meta-repo document, and a pointer to an unreachable file tells an agent that a constraint exists without telling it what the constraint is, which invites a guess in exactly the situation the rule exists to prevent. Canonical text and reasoning: `docs/conventions/non-public-sources.md` and ADR 012 in the meta-repo (`decasamerlo/nesto`).

Nesto is public; the codebases its docs draw precedent from are not.

- **Verify before naming.** Any repository named in published text must be public: `gh repo view <owner>/<repo> --json isPrivate`, reject on `true`. Read the field — a lookup that merely succeeds proves nothing, because an agent runs authenticated as the author and sees a private repository as an entirely ordinary one.
- **Cite by shape, never by measurement.** Never publish identifiers, verbatim quotation, or counts of implementations, services, or references taken from a non-public codebase. State precedent as direction only — "the dominant approach", "a minority pattern".
- **Surfaces:** commit messages, files, issue bodies, issue comments, PR bodies, PR reviews.
- **Fires twice:** when drafting any of the above, and as a checklist item in every review pass — including over text a human wrote.
- **On a trip:** write the generic form and say that you did. Don't stall for a decision, and don't substitute silently.
