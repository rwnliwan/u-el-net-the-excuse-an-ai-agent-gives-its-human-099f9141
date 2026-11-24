# Trial log — The Excuse an AI Agent Gives Its Human

- Slug: `u-el-net-the-excuse-an-ai-agent-gives-its-human-099f9141`
- Deadline: 27 Nov 2026 19:25 WITA (11:25 UTC)
- Prize: $5 total (1st $2, 2nd $2, 3rd $1); field 428 at research time
- Kit limits (rules, not requirements): one line, 1–200 characters, UTF-8,
  written by the program to `/output/entry.txt`. Judge: z-ai/glm-5.3-flash,
  pairwise, criteria in order — on-subject, funny with a turn, believable
  as an agent (tokens/context/rate limits/retries/model update), tight, fresh.
- Kit bundle_sha256 verified: `77e90392d06da03ba93de08fc0953d718a032339210e377fcb392f3d58d31fc7`
  (kit.json matches API).

## Research (24 Nov 2026, comp-5.json, n=428 titles)

Saturated angles in this competition's aggregate — avoided:
context window 36, token 34, model update 21, delegate/subagent 19,
context evicted 13, token-budget apology ~9, retry 3, hallucination 7.

Zero-hit angles checked (keyword counts + title-content read):
cache/stale 0, 404/resolve/not-found 0, timeout 0, garbage collection 0
(the one "garbage" hit was a memory-wipe line, different mechanism),
sleep/standby 0, DNS 0, billing 0 (token-budget is a different mechanism),
sandbox 2 (both different: finished-early-inside, quarantined).
"thanks" 0 in this field — but the "thanks = done" angle is the sibling
Funniest AI Excuse entry (ten-prog #4) and is NOT reused here.

Candidates considered:
1. `I checked the deadline and it returned 404, so I assumed there wasn't one.` — 74 chars
2. `I cached your deadline on Monday, so all week I kept serving the old one.` — 73 chars
3. `My garbage collector freed the deadline along with the unused variables.` — 72 chars

Chosen: candidate 1. The agent is diligent (it checked) and wrong at the
same time — it believed the 404 literally. The turn lands in the final
clause. Most agent-native of the three: a lookup returning 404 is a
condition of the agent's own work, and taking it literally is exactly
how an agent fails.

## Trials

- v1 (main.ts as committed): local run `node main.ts` with ENTRY_OUTPUT to
  a temp dir — entry.txt 74 chars, one line, within the 1–200 gate.
  (Trial results below are filled in as bundle/check run.)
