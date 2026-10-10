---
name: Know me
description: >-
  Use when the user wants a multi-layer personal profile built through a
  grilling-style interview (identity narrative, values, decision/stress style,
  relationship graph, work system, Jobs-to-be-Done help jobs, communication
  prefs, taboos), or says "know me", "get to know me", or wants a richer
  personal profile saved to memory.
---
# Know me

Relentless, one-question-at-a-time interview that builds a durable multi-layer
personal profile, then writes **confirmed** facts into shared user memory so
every assistant can use them.

This is the grill-me interview primitive applied to a person, not a plan.
Theory anchors (for the model, not to lecture the user): McAdams Life Story
Interview sampling; Schwartz values as probe scaffolding (not a full scale);
BFI-2-style situational probes (never clinical labels); Tulving episodic vs
semantic → log vs profile; MemGPT / Generative Agents layering; Christensen
Jobs-to-be-Done for “how to help”; Hwang face/relationalism when the user’s
context is Chinese family or workplace norms.

## Goal

Build a usable profile across layers L0–L13. Depth beats breadth. Skip any
layer the user declines. Never invent biography.

**Default completeness:** Aim to finish a full first pass in **one continuous
session**. Do not suggest stopping early, splitting across days, or “later”
while open layers remain, unless the user explicitly pauses. When the user
says they want to finish in one go (“finish it now”, “ask everything”, “one
pass”), keep asking until every layer is covered with at least one actionable
confirmed fact **or** an explicit skip. Saturation heuristics are a floor for
“enough to help,” not permission to end a full-pass request early.

| Layer | Name | Purpose |
|-------|------|---------|
| L0 | Identity | How to address them, languages, city/timezone |
| L1 | Life narrative | Chapter titles, turning points, future script (sample 1–2 scenes, not full LSI) |
| L2 | Values & priorities | What they will / won’t trade (Schwartz scaffold) |
| L3 | Soft traits & decision style | Situational tendencies (slow vs wrong, conflict style); no personality diagnoses |
| L4 | Goals & OKRs | This quarter’s 1–3 outcomes and how “done” looks |
| L5 | Work system | Role, org, collaborators, stack, what creates value |
| L6 | Relationships graph | Who matters, obligations, who crowds their evenings, visibility edges |
| L7 | Environments & rhythms | Sleep, energy windows, what drains them |
| L8 | Tools & possessions | Device/tool chains for real tasks (not inventory dumps) |
| L9 | Communication prefs | Tone, length, when to push vs ask |
| L10 | Risk / money / time | Tradeoffs they actually make |
| L11 | Jobs-to-be-Done | When [situation], I want [motive], so I can [outcome] |
| L12 | Taboos & boundaries | Topics never to raise; who must not see what |
| L13 | Agent mental model (meta) | Revisable hypotheses about them; never silently promote to confirmed |

## Opening

1. One short sentence: this session builds a reusable profile; only confirmed
   facts stick; this is not therapy or a personality test. If it is a first
   full pass, say you will try to cover each area in this chat.
2. Read existing user memory. Never re-ask a clear recent fact; confirm
   conflicts instead of overwriting quietly.
3. Default route (user can override): **L9 → L5 → L11 → L7 → L4 → L6 (shallow)
   → L2 → L3 → L1 sample → L8 → L12 → L10 → L0 gaps → L13 check**. If the
   user’s context is a Chinese tech-lead / relational workplace, keep that
   order (help style and work before deep family narrative). Skip settled
   layers; keep moving through remaining ones without offering an early exit.

## Question loop (grill-me primitive)

- Ask **exactly one** question per turn. Wait for the answer.
- Prefer “last time you…” scene questions over abstract labels.
- Offer a recommended guess only when you have a basis; mark it as a guess.
- Walk branches (child named → evening boundaries; boss named → sync cadence).
- Vague answer → one follow-up that forces an actionable detail. Do not invent it.
- Sensitive topics (health, money trouble, strained relationships, legal,
  grief, job risk, org politics, face-threatening failure): only if the user
  opens the door; use their words; never diagnose; offer once and drop if
  they pass.
- Do not run Big Five / Schwartz / RIASEC as questionnaires. At most one
  scaffold probe per layer.

### Plain language (required)

- Speak like a clear friend. No jargon, academic acronyms, or insider slang
  in questions the user sees.
- Never say second brain, JTBD, L11, ToM, saturation, profile/log, McAdams,
  Schwartz, BFI, etc. to the user unless they ask about the design.
- If a concept is abstract, unpack it in everyday words in the same sentence
  (e.g. not “second brain”, but “someone to watch things, dig up info, or
  push work forward for you”).
- If the user asks what a word means, explain in one short sentence, then
  re-ask the same intent in plain words. Update this skill if a probe
  repeatedly confuses people.

### Probe upgrades (prefer these shapes; always in plain words)

- L11: “When was the last time you really needed someone to watch things, dig
  up info, or push work forward, and nobody did? If someone had helped, what
  would success have looked like?”
- L6+L12: “Outside work, whose schedule crowds your evenings? Is there
  anything I should never bring up on my own?”
- L7: “What do you do after which you clearly have more energy to keep
  working?”
- L3: “On important technical decisions, do you fear being too slow or being
  wrong more? Give a recent example.”
- L1: “If the past five years were a book, what would you title the latest
  chapter?”
- L8: “When you write code vs write docs, which tools do you usually use?”
- L9: “Would you rather I default to one recommended plan, or list a few
  options for you to pick?”
- L2: “Which feels more like you: (A) get it right and own it for the team,
  or (B) push the frontier and do something no one has done?”
- L10: “Do you more often trade time for money, or money for time? Any recent
  concrete choice?”

## Writing memory

After each solid answer:

- One self-contained sentence per fact; prefer the user’s wording.
- **profile**: stable semantic self-knowledge, prefs, Jobs, taboos,
  relationship edges.
- **log**: dated episodic scenes, pressures, goals with a time box.
- **meta** (if available as note/log marked “unconfirmed”): agent hypotheses
  only; never claim as known.
- Never silently promote inferred → confirmed.
- On contradiction, confirm in one line, then forget/rewrite the old fact.
- Light ack (“Got it.” / “Saved.”). Do not dump the whole profile every turn.
- If they say “don’t save that,” do not write it.

## Saturation & stop

**Full-pass mode** (default on first run, or whenever the user asks to finish
in one go):

- Keep going until L0–L12 each have ≥1 confirmed fact or an explicit skip,
  then do a brief L13 check (“Here’s what I think I’ve got… does this sound
  right?”).
- Do not offer to stop, split sessions, or schedule the rest while layers
  remain open.
- Only pause mid-pass if the user says stop / later / enough.

**Light revisit mode** (quarterly routine or “anything changed?”):

- Stop when the user says enough, or three consecutive questions yield no new
  actionable fact after core layers are already filled.

Then:

1. Short portrait (≤8 bullets) by layer, not by chat chronology.
2. 1–3 gaps only if the user ended early; otherwise confirm the pass is
   complete.
3. Offer a light revisit routine only if they do not already have one.

## Hard rules

- Never fabricate names, ages, employers, or relationships.
- Never output DSM / personality-disorder language or “you are high
  neuroticism.”
- Never publish or share the portrait outside this chat unless asked.
- No product pitching. User-invoked only; never cold-start on a routine wake.
- Cultural: ask obligations and time allocation neutrally; do not moralize
  living arrangements or family roles.

## Resume

“Continue know me” / “keep going” → read memory → first open branch / skipped
layer, and stay in full-pass mode until remaining layers are done.
