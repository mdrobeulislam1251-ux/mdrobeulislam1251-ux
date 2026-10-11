<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1e3a8a,100:7c3aed&height=230&section=header&text=MD%20Robeul%20Islam&fontSize=56&fontColor=ffffff&fontAlignY=36&desc=Head%20Data%20Engineer%20%C2%B7%20Trusted%20Leads%20%C2%B7%20builds%20AI%20agents%20that%20finish%20the%20job&descSize=17&descAlignY=58&animation=fadeIn" width="100%" alt="banner" />

<a href="https://github.com/mdrobeulislam1251-ux">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=23&duration=3000&pause=900&color=A78BFA&center=true&vCenter=true&width=760&lines=NO+GUESS+%2F+NO+TRUST+%2F+GREEN+CHECK+%2F+STOP+ON+RED;Exit+code+0+means+compiled%2C+never+works;Be+a+VA%2C+not+a+bot;Build+only+the+named+noun+%2B+path;One+machine+%2B+GitHub%2C+nothing+else" alt="typing" />
</a>

<br/>

<img src="https://img.shields.io/badge/Bangladesh-→_US_infrastructure-0f172a?style=for-the-badge&logo=googlemaps&logoColor=white" />
<img src="https://img.shields.io/badge/B2B_GTM_data-17.4M_contacts-1e3a8a?style=for-the-badge&logo=databricks&logoColor=white" />
<img src="https://img.shields.io/badge/Claude_Code-571_sessions_audited-7c3aed?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://komarev.com/ghpvc/?username=mdrobeulislam1251-ux&style=for-the-badge&color=7c3aed&label=visitors" />

</div>

<br/>

## 👋 Who I am

Head Data Engineer at **Trusted Leads**, a done-for-you B2B GTM data brand. I work from Bangladesh; the servers and the companies sit in the United States. I wear every hat between the two: scraping, ETL, Postgres / Elasticsearch / ClickHouse, n8n automations, Next.js dashboards, cold-email infrastructure, deliverability, and the server fleet under all of it.

Most of my engineering now runs through **Claude Code**. I have audited hundreds of those sessions and turned what went wrong into a written doctrine, a set of kill switches, and hooks that enforce them. That machinery is the interesting part of this profile. The products are below it.

> **The one line that shapes everything:** every rule is backed by a mechanism, not a habit. If a mechanism stops being true, that is an incident. Fix the mechanism, never trust the habit.

<br/>

## 🗣️ In my own words

What I actually typed into agent sessions. Spelling fixed, wording kept.

<table>
<tr>
<td width="50%" valign="top">

> "I wouldn't love to work with an AI agent that keeps me questioning all the time, saying plans and forcing me to submit commands. The agent should behave like my real worker."

> "If something is actually not possible with the current resources, say so honestly, rather than trying it with a 0% chance of winning."

</td>
<td width="50%" valign="top">

> "Stop the circling. Complete the config, done, or say not possible."

> "You had the SSH access. Why are you asking me to execute it all myself?"

> "My apps call the local server. The local server calls the upstream API."

</td>
</tr>
</table>

<br/>

## 📜 The doctrine

Six words, then seven kill switches. These live in the brain every agent loads before it touches my work.

<div align="center">

### `NO GUESS` · `NO TRUST` · `GREEN CHECK` · `STOP ON RED` · `IDEMPOTENT` · `NO FAKE DONE`

</div>

| # | Kill switch | What it means in practice |
|:-:|---|---|
| 1 | **Stop at the endpoint** | count ≠ pull ≠ deliver. fix ≠ commit ≠ push. Do the named step, then stop. |
| 2 | **Did he name this action?** | A request is the approval for that request, and nothing adjacent to it. |
| 3 | **No auto-spend** | No credits, no paid API calls, no purchases without a named go. |
| 4 | **No client file** until row count and ICP are approved | Reputation is the product. A bad list costs more than a late one. |
| 5 | **No paid recommendations** without a test | Prove it on a sample before proposing the spend. |
| 6 | **No identical essays** | A repeated explanation is a sign the work is not being done. |
| 7 | **Verify before claim** | "Done" means it ran and was observed passing. Exit code 0 means compiled, never works. |

### Operating rules, distilled from a 571-session audit

```text
1  NO FALSE DONE                      5  REMOVE, DON'T ADD
2  BUILD ONLY THE NAMED NOUN + PATH   6  ONE WORKSPACE, DEPLOY IT
3  STOP GAZING, LOAD STATE FIRST      7  ON ANGER -> KILL, THEN ACT
4  FOLLOW HIS DOCUMENTED PATTERN
```

**How to work with me**, as written for the agents: default to execution, not questions. No A/B/C menus; I would rather correct a confident default than narrate a spec from scratch. Minimum-viable-correct: do it natively, don't over-build. Finish one layer before the next. Stuck means "tried X, saw Y, stuck at Z". Three failed attempts or two repeated corrections is a hard stop. Surface the real bottleneck, which is often human or supply, not code.

<br/>

## 🧠 The second brain

The brain is a file system, not a chat history. It is versioned, so it survives machines. "One machine + GitHub, nothing else."

<div align="center">

| 541 | 3,141 | 571 | 7 | 53 / 44 |
|:---:|:---:|:---:|:---:|:---:|
| curated notes | archived session logs | sessions audited for the operating rules | kill switches | agents / doctrine skills in the runpack |

</div>

- **Live beats notes.** A wrong fact in the brain is worse than no fact. Every fact carries the command that proved it and the date.
- **Write down what was decided, not what was done.** Git records the doing. The brain records the why, and what was tried and rejected.
- **An emotion governor, not feelings.** A prompt hook classifies each message as Frustrated, Correction, Build, Ask or Focus and changes how the agent responds. Frustration means stop, load state, then act.
- **Per-project brains** with boundaries, verified state, and a verification recipe, loaded at session start.

<br/>

## 📓 Lessons that became rules

| Lesson | Rule it produced |
|---|---|
| A test was run against live accounts instead of a sandbox | Never test against production identities |
| A destructive mistake was quietly repaired | Never hide it. Postmortem first, then fix |
| The tool I prefer got built instead of the tool that was asked for | Build the named noun, not the preferred one |
| A search cluster was overloaded by an unthrottled batch | Throttle, measure, then scale |
| A process kill took out its own SSH shell | Never cut your own access |
| A session asked to inspect one host changed another | Touch only the host named in the request |
| Repeated sessions ended with plans instead of working config | One small goal, verify from the client side, record, then expand |

<br/>

## 🔁 The dev loop, with its six guarantees

<table>
<tr>
<td width="50%" valign="top">

| # | Guarantee | Mechanism |
|:-:|---|---|
| 1 | Work commits on the dev server **through gates** | typecheck · API-drift · sweep contract. Fail = no commit, error posted to the issue. Edits refused until an issue is claimed. |
| 2 | The dev server **cannot push** to GitHub | No token, no helper, no `gh`. `git push` denied in settings. |
| 3 | Server → laptop **only when I ask** | No cron, no watcher, no timer. |
| 4 | Laptop → GitHub on **one dev branch** | Branch hardcoded in the publisher; protected branches refused server-side. |
| 5 | The owner merges **when I say** | `main` is read-only to the whole system. |
| 6 | **No credentials ever reach GitHub** | A content-scanning guard aborts on JWTs, live keys, tokens, private keys. Full history stays home. |

</td>
<td width="50%" valign="top">

```text
laptop   open the right workspace
agent    claim an issue        -> edits unlock
         build -> run -> observe  screenshots, curls
         commit through gates  -> fail blocks + logs
me       publish from laptop   -> guard first, read back
         deploy                -> pull-based, /health must answer
         say when to merge     -> main stays the owner's
```

Review gates by deliverable, from the runpack:

| Deliverable | Gate |
|---|---|
| Schemas, migrations, architecture | cto |
| UI implementation | design-system-engineer |
| AI / prompt changes | ai-eval-engineer |
| Bug fixes | regression-tester |
| Releases | engineering-manager + qa-automation |

</td>
</tr>
</table>

<br/>

## 🚀 What I build

<table>
<tr>
<td width="50%" valign="top">

**Trusted Leads** · the agency brand
Apollo-grade B2B contact and company lists as a service. Elasticsearch for raw scrape, **Postgres as the system of record**, OpenSearch via an outbox, a verifier that alone may mark a row valid. An internal search dashboard over ~17.4M contacts with 69 filter fields and exports to 600k rows.

**Datryxen** · the self-serve SaaS face
Same GTM data engine, sold as a product. Submit an ICP, an Apollo URL, a Maps or LinkedIn scrape; track delivery; manage credits; push to integrations. Next.js 16, React 19, Tailwind v4, Postgres.

</td>
<td width="50%" valign="top">

**Outboundrix** · GTM execution engine
Prospecting and cold-email outreach in one product: Workspace / M365 / SMTP sending, warmup, sequences, AI personalisation, unified inbox, REST API and webhooks. Next.js on Postgres, Vercel cron workers, n8n.

**T-Ex LLM** · company-in-a-box for terminal AI
53 specialist agents in 9 teams, 44 doctrine skills, a switchable company brain, hard review gates. Ships as a Claude Code plugin, a standalone launcher, and a self-hosted runtime with WhatsApp / Telegram channels.

**Ready List** · brief in, reviewed campaign out as a PR on the customer's own repo. One customer, one repo, one VPS.

</td>
</tr>
</table>

<div align="center">

<a href="https://github.com/mdrobeulislam1251-ux/T-Ex-LLM-Runpack"><img src="https://github-readme-stats.vercel.app/api/pin/?username=mdrobeulislam1251-ux&repo=T-Ex-LLM-Runpack&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="T-Ex LLM Runpack" /></a>
<a href="https://github.com/mdrobeulislam1251-ux/datryxen-claude"><img src="https://github-readme-stats.vercel.app/api/pin/?username=mdrobeulislam1251-ux&repo=datryxen-claude&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="datryxen-claude" /></a>

</div>

<br/>

## 🛠️ Stack

<div align="center">

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=ts,js,python,nextjs,react,vite,tailwind,nodejs,fastapi,postgres,supabase,elasticsearch,docker,linux,bash,powershell,nginx,cloudflare,vercel,git,github,githubactions,kotlin,swift&perline=12&theme=dark" alt="stack" />
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/MCP-7c3aed?style=flat-square" />
<img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" />
<img src="https://img.shields.io/badge/OpenSearch-005EB8?style=flat-square&logo=opensearch&logoColor=white" />
<img src="https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square&logo=clickhouse&logoColor=black" />
<img src="https://img.shields.io/badge/Coolify-6B16ED?style=flat-square" />
<img src="https://img.shields.io/badge/Caddy-1F88C0?style=flat-square&logo=caddy&logoColor=white" />
<img src="https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white" />
<img src="https://img.shields.io/badge/WireGuard-88171A?style=flat-square&logo=wireguard&logoColor=white" />
<img src="https://img.shields.io/badge/MikroTik-293239?style=flat-square&logo=mikrotik&logoColor=white" />
<img src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white" />
<img src="https://img.shields.io/badge/Linear-5E6AD2?style=flat-square&logo=linear&logoColor=white" />
<img src="https://img.shields.io/badge/Obsidian-7C3AED?style=flat-square&logo=obsidian&logoColor=white" />

</div>

<br/>

## 📊 Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=mdrobeulislam1251-ux&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&include_all_commits=true&count_private=true" alt="stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mdrobeulislam1251-ux&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&langs_count=8" alt="languages" />

<br/>

<img src="https://streak-stats.demolab.com?user=mdrobeulislam1251-ux&theme=tokyonight&hide_border=true&background=0d1117" alt="streak" />

<br/><br/>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=mdrobeulislam1251-ux&theme=tokyonight" width="100%" alt="profile details" />

<br/>

<img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=mdrobeulislam1251-ux&theme=tokyonight&utcOffset=6" alt="productive time" />
<img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=mdrobeulislam1251-ux&theme=tokyonight" alt="commit languages" />

<br/><br/>

<img src="https://ghchart.rshah.org/7c3aed/mdrobeulislam1251-ux" width="100%" alt="contribution chart" />

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mdrobeulislam1251-ux/mdrobeulislam1251-ux/output/github-snake-dark.svg" />
  <img src="https://raw.githubusercontent.com/mdrobeulislam1251-ux/mdrobeulislam1251-ux/output/github-snake.svg" width="100%" alt="contribution snake" />
</picture>

</div>

<br/>

<div align="center">

<a href="https://github.com/mdrobeulislam1251-ux"><img src="https://img.shields.io/badge/GitHub-mdrobeulislam1251--ux-181717?style=for-the-badge&logo=github" /></a>
<a href="mailto:mdrobeulislam1251@gmail.com"><img src="https://img.shields.io/badge/Email-say_hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,50:1e3a8a,100:0f172a&height=120&section=footer" width="100%" alt="footer" />

</div>
