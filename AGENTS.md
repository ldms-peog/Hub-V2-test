# Repository conventions — CISO AI Hub V2

Codex: read this file before any task in this repository.

## Non-negotiable constraints

- **Vanilla only.** HTML, CSS and JavaScript. No framework, no CDN, no npm
  dependency, no build step.
- **Zero network.** The page must never issue a request. No fonts, no
  analytics, no images from the web. Everything inline or base64.
- **Must work from `file://`** and inside a sandboxed iframe preview.
  Wrap `localStorage` in `try/catch`; degrade silently.
- **Single file output.** `index.html` contains everything.

## Content lives in CONFIG, never in the markup

All editable content sits in one `CONFIG` object at the top of the
`<script>`, sourced from `docs/content.json`. A non-developer must be able
to add a PSL, change a link or reword a step without touching logic.

No magic numbers. No hardcoded label inside a function.

## The agent adapter layer

Four AI agents support the lifecycle (see `docs/lifecycle.md`). Three are
not published yet. Their behaviour is implemented locally behind a stable
interface so the real agent can be swapped in later.

Every agent exposes the same shape: `{ id, label, mode, status, deeplink,
run(state) }`. The UI calls `AGENTS.x.run(state)` and renders the result —
it never contains agent logic itself.

Changing an agent from local to real must require editing `AGENTS` only.

## Vocabulary

The user never sees the word "agent" when `status === 'local'`. The app is
simply helpful. Agents are named explicitly only when a real one is
reachable.

Use the exact lifecycle step names from `docs/lifecycle.md`. Do not invent
synonyms (no "Frame", "Assess", "Scale").

## Design system

| Token | Value |
|---|---|
| navy | `#0B1B3A` |
| navy-2 | `#13284F` |
| teal | `#00C2A8` |
| background | `#F4F6FB` |
| card | `#FFFFFF` |
| border | `#E1E7F0` |
| ink | `#12203A` |
| muted | `#66738A` |
| amber | `#E0932B` |
| green | `#1E9E63` |
| red | `#C0392B` |

Font: Segoe UI / system stack. Radius 10-12 px. Transitions 180-280 ms,
`cubic-bezier(.4,0,.2,1)`. Restrained and executive. No emoji.

## Accessibility

Keyboard navigable end to end. Visible focus states. ARIA labels on the
stepper and the gauge. Contrast AA. Responsive to 900 px, single column
below.

## Working style

Small tasks, one concern per diff. Comment each block. Prefer readability
over cleverness. Under 1500 lines total.

## Git workflow
Never commit directly to `main`.
Always create a branch named `codex/<short-task-name>` and open a pull request.
