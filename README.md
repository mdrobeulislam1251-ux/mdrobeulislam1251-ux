# MD Robeul Islam

I build AI agents that do real engineering work, and the guardrails that make their output trustworthy.

Most of my day is spent running Claude Code sessions against live servers, data pipelines and product codebases. The interesting part is not the prompt. It is the machinery around the agent: what it is allowed to touch, what proves its work, and what stops a mistake from leaving the building.

This page is the short version of that machinery.

---

## The idea in one line

**Every rule is backed by a mechanism, not a habit.** If a mechanism stops being true, that is an incident. Fix the mechanism, never trust the habit.

---

## Six guarantees the dev loop enforces

| # | Guarantee | What enforces it |
|---|---|---|
| 1 | All development commits on the dev server, through gates | A `commit` command runs the workspace's gates (typecheck, API-drift check, any declared sweep contract). A failure blocks the commit and posts the error to the tracking issue. Code edits are refused at the tool layer until an issue is claimed, and an issue can only be claimed inside its own workspace. |
| 2 | The dev server can never push to GitHub | No credential helper, no stored token, no `gh` on the box. `git push` is denied in every workspace's settings. A push attempt gets a 401. |
| 3 | Server to laptop only when I ask | Nothing automatic exists. No cron, no watcher, no timer. |
| 4 | Laptop to GitHub: one dev branch only | The branch name is hardcoded in the publish script. The server-side pipeline refuses commits on `main`, `master`, `staging` and friends. |
| 5 | The product owner merges when I say | `main` is read-only to this whole system. The only interaction with it is a read-only report of what landed there. |
| 6 | No server credentials ever reach GitHub | A content-scanning guard runs on every publish. It aborts on secret material (JWTs, live API keys, signing secrets, tokens, private keys). The app publish is a filtered single-commit export, so the server's full history never leaves the server. |

Measured, not assumed: on the last audit the guard cleared every tracked file and withheld zero. It still runs on every push, because that is what proves the zero.

---

## The loop, end to end

```
laptop:  open the right workspace            brain, gates and tracking live there
agent:   claim an issue                      unlocks edits for that workspace only
         build -> run -> observe             screenshots for UI, curls for APIs
         commit through the pipeline         gates run; failure blocks and writes to the issue
me:      publish from the laptop             dev branch only, guard first, read back after
         deploy                              pull-based, read-only key, must answer /health
         say when to merge                   main stays the owner's
```

A commit that passes leaves the issue **In Review**. That means the work is waiting for my publish, not that it shipped.

Failure is routed straight back into coding with the evidence attached:

- **Gates fail**: the commit never happens, the issue gets a rework label and the error output as a comment, and it sorts to the top of the queue.
- **Wrong branch**: refused before anything is staged.
- **Secret found**: the push aborts before the fetch. A secret is never merely withheld. It is removed.
- **Work left on the floor**: a stop hook notices a claimed issue with uncommitted files and says so.

---

## What the agent is told

These are the standing instructions in every workspace. They are not suggestions.

1. **Build, do not describe.** A write-up is not a deliverable unless docs were what was asked for.
2. **Decide and do.** Pick, proceed, report. Stop only for a decision nobody else can make: a missing secret, or an irreversible external action.
3. **Never fake it.** "Done" means it ran and was observed passing. "Should work" is not done. If it was not run, say so. This overrides autonomy.
4. **Answer the question asked.** A scoped request does not become an audit. Scope creep buries the one finding that mattered.
5. **This is dev, not production.** Publishing is a deliberate act by a person.
6. **Nothing is hosted on the laptop.** I work from several machines. Anything bound to one of them is invisible from the others.

---

## How I treat servers

- **Live beats notes.** Docs go stale. Confirm the host before acting on it, and check its identity after connecting. If it does not match, stop.
- **Report only what was verified.** Every claim is "ran it", "read it", or marked unverified. "Healthy" only comes from a check run in this session.
- **Stay in scope.** Touch only the hosts named in the request. A doc that lists a host does not authorize work on it. This rule exists because it was once broken.
- **Read-only by default.** To change something: read its state, take a timestamped backup, write down the rollback, make one change, validate, verify by observing the result, log it.
- **Don't cut your own access.** Never restart SSH or the VPN on the box you are connected through.
- **Never bind internal services to all interfaces.** Loopback or the private network, nothing else.
- **Secrets stay out of output.** Record names and paths, never values.

---

## Memory that survives the session

The agent's brain lives on the server, inside the workspaces, not in chat history. Every turn is captured, sessions that die without a clean exit are distilled at the next start, and retrieval ranks the whole episode corpus by relevance rather than recency. Decisions are written down separately from actions: git already records what was done, but it cannot tell you six weeks later why something was chosen or what was tried and rejected.

---

## Things I build

| | |
|---|---|
| [T-Ex LLM Runpack](https://github.com/mdrobeulislam1251-ux/T-Ex-LLM-Runpack) | A company-in-a-box for terminal AI sessions: 53 specialist agents in 9 teams, 44 doctrine skills, a switchable company brain, and hard review gates. |
| [T-Ex LLM Agent](https://github.com/mdrobeulislam1251-ux/T-Ex-LLM---Agent) | The self-hosted agent host. One-command install on your own VPS and your own Claude subscription, with chat channels and an ICP, lead-cleanup and n8n skill pack. |
| [datryxen-claude](https://github.com/mdrobeulislam1251-ux/datryxen-claude) | Headless Claude Code orchestration on a subscription, no API key: classify, route, execute, report. |

Private work, in the same style: a B2B lead-data platform with a multi-workspace dev pipeline (web app, API server, MCP server, mobile and native apps), a contact-search dashboard over tens of millions of records, scraper orchestration, and a self-hosted n8n stack.

---

## Stack

Claude Code and agent harnesses · TypeScript and Next.js · Python and FastAPI · Postgres and Supabase · Elasticsearch and OpenSearch · n8n · Linux, systemd, Caddy and Tailscale · Linear for intent, GitHub for published code
