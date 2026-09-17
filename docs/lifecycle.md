# The AI use case lifecycle — reference

Source: *[STLA] - CISO TOM 2026 - AI for Cyber governance framework*.
This is the canonical version. Any other naming (including the Microsoft
"Ideation & Intake / Qualification & Priority / Build & Experiment /
Governance & Control / Deploy & Scale" sequence) is **not** to be used.

---

## The five steps

| # | Step | Owner |
|---|---|---|
| 1 | Ideation & self-assessment | AI end-user |
| 2 | Value & feasibility assessment | Cyber Data & AI Factory PSL |
| 3 | Design & development | AI end-user |
| 4 | Testing | Cyber Data & AI Factory PSL |
| 5 | Go-live & feedback assessment | AI end-user |

## Governance gates

Two meeting bodies carry the gates:

- **AI catch-up meeting per PSL** — shares and aligns on AI opportunities
  within the PSL, validates design, validates testing results, steers
  deployment inside the PSL.
- **AI coordination committee** — gives GO / NO-GO for the testing phase,
  GO / NO-GO for the design phase, GO / NO-GO for go-live, and monitors all
  AI use cases across CISO (continue, remediate, retrain, decommission).

| After step | Gate |
|---|---|
| 1 | Share and align on AI opportunities within the PSL |
| 2 | GO / NO-GO for the design phase |
| 3 | Validate the design of the AI use case within the PSL |
| 4 | Validate the results of the testing phase, then GO / NO-GO for go-live |
| 5 | Monitor — continue, remediate, retrain or decommission |

> **TO BE COMPLETED.** The formal acceptance criteria (definition of done)
> behind each gate are not yet defined. The readiness score weights in the
> app are a provisional stand-in and must be revisited once published.

## Step 5 — detail available

Go live with the use case and drive its adoption within the team (training
and awareness sessions). Collect feedback on adoption, business and value
outcome, and effectiveness, then report to the Cyber Data & AI Factory PSL.
Scale, improve or retire the use case based on that feedback assessment,
together with the Cyber Data & AI Factory PSL.

---

## The four supporting AI agents

| Agent | Mode | Status | What it does |
|---|---|---|---|
| **AI Ideation / Intake Agent** | Context-based | ⚠ conflicting — see below | Chat agent in M365 Copilot that takes your inputs, structures the idea and logs it into the AI use case tracker |
| **AI Build & Deploy Agent** | Context-based | In progress | Chat agent in M365 Copilot that assists the use case owner through building, testing and deploying the solution |
| **AI Value Assessment Agent** | Always on | In progress | Prompt-based agent with skills to assess value continuously across every step of the lifecycle |
| **AI Learning Agent** | Always on | In progress | Prompt-based agent with skills to help the owner and answer questions throughout the lifecycle |

**Context-based** — helpful during precise steps of the lifecycle.
**Always on** — used at any time to provide tips.

### ⚠ Status conflict to resolve

The governance framework marks the Ideation / Intake Agent as **live**.
The AI use case tracker records it as **AI-86 "Cyber AI Ideation Agent",
status In POC**, owner Céline, Copilot Studio, with the note
*"07/09 — Agent is in draft in Copilot Studio, working to publish"*.

Until resolved, the app treats all four agents as `status: 'local'`.

### Related agents in the tracker

- **AI-88 · AI-First Process Redesign** — In POC, Céline, Copilot Studio
- **AI-89 · Business Value Assessment** — In POC, Annette / Emma, Copilot
  Studio *(uses the Copilot Studio App feature, currently in preview)*

> The app's readiness scoring should eventually align with AI-89 rather
> than run a parallel method.

---

## Agent deeplinks

| Agent | Deeplink |
|---|---|
| Ideation / Intake | **TO BE PROVIDED** |
| Build & Deploy | **TO BE PROVIDED** |
| Value Assessment | **TO BE PROVIDED** |
| Learning | See `LINKS.learning_agent` in `content.json` |
