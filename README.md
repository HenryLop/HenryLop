I'm a Salesforce architect who builds agent systems for my own work. These repos are the parts I ended up reusing: guardrails that stop an agent from acting without a human, evals that check its output, and the plumbing to keep many sessions straight. Each one runs from a single command with sample data, and each README has a Results section with counts from my own use.

More about them: https://made-by-asking.pages.dev/showcase/

## Guardrails

- [prod-lockdown-guards](https://github.com/HenryLop/prod-lockdown-guards): writes to production blocked until a human clicks. 4,509 tool calls checked in three days, 11 denied.
- [consent-tokens](https://github.com/HenryLop/consent-tokens): typed approval for payments and phone access. 30,323 checks across the two guards, 66 denials.
- [studio-credit-guard](https://github.com/HenryLop/studio-credit-guard): a paid generation runs only after a typed approval. 32 requests filed, 12 never approved, and none of those spent a credit.

## Verification

- [qa-loop](https://github.com/HenryLop/qa-loop): build, then an adversary tries to break it. Of 62 runs that passed, 43 passed only after a failing first round.

## Context and memory

- [dominio-router](https://github.com/HenryLop/dominio-router): injects only the area files a prompt touches. Context was added on 92 of 902 prompts.
- [thread-notes](https://github.com/HenryLop/thread-notes): one note per work item with fixed fields and a checker. 65 notes, 64 done.
- [whatsapp-memory-mcp](https://github.com/HenryLop/whatsapp-memory-mcp): local search over exported chats as an MCP server. 18 tests; it has no usage numbers yet.

## Running many agents

- [session-board](https://github.com/HenryLop/session-board): every Claude Code session as a card. 1,835 session transcripts read over two months.
- [usage-brake](https://github.com/HenryLop/usage-brake): a daily allowance with alarm levels for plan usage. 58 alarm events over 40 days.
- [release-pollers](https://github.com/HenryLop/release-pollers): one poller per awaited change, one email, then it stops. 56 runs, 1 email sent.

## Live calls

- [live-call-coach](https://github.com/HenryLop/live-call-coach): cards for an interview or meeting as it happens. 19 tests; the latencies in the demo are simulated, so there are no field numbers.
