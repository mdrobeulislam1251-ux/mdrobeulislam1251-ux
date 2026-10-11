<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1e3a8a,100:7c3aed&height=220&section=header&text=MD%20Robeul%20Islam&fontSize=56&fontColor=ffffff&fontAlignY=38&desc=AI%20agents%20that%20do%20real%20engineering%20work%2C%20and%20the%20guardrails%20that%20make%20them%20trustworthy&descSize=17&descAlignY=58&animation=fadeIn" width="100%" alt="banner" />

<a href="https://github.com/mdrobeulislam1251-ux">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=3200&pause=900&color=A78BFA&center=true&vCenter=true&width=720&lines=Agent+harnesses+with+hard+gates;Build%2C+do+not+describe;Decide+and+do.+Never+fake+it.;Every+rule+is+a+mechanism%2C+not+a+habit;Live+beats+notes." alt="typing" />
</a>

<br/>

<img src="https://img.shields.io/badge/Claude_Code-agent_harnesses-7c3aed?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/B2B_data-pipelines-1e3a8a?style=for-the-badge&logo=databricks&logoColor=white" />
<img src="https://img.shields.io/badge/self--hosted-infra-0f766e?style=for-the-badge&logo=linux&logoColor=white" />
<img src="https://komarev.com/ghpvc/?username=mdrobeulislam1251-ux&style=for-the-badge&color=7c3aed&label=visitors" />

</div>

<br/>

## 🧠 What I do

I run Claude Code sessions against live servers, data pipelines and product codebases. The interesting part is not the prompt. It is the **machinery around the agent**: what it may touch, what proves its work, and what stops a mistake from leaving the building.

> **Every rule is backed by a mechanism, not a habit.** If a mechanism stops being true, that is an incident. Fix the mechanism, never trust the habit.

<br/>

## 🛠️ Stack

<div align="center">

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=ts,nextjs,react,nodejs,python,fastapi,postgres,supabase,elasticsearch,docker,linux,bash,nginx,cloudflare,git,github,githubactions,vercel,kotlin,androidstudio&perline=10&theme=dark" alt="stack" />
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" />
<img src="https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white" />
<img src="https://img.shields.io/badge/Caddy-1F88C0?style=flat-square&logo=caddy&logoColor=white" />
<img src="https://img.shields.io/badge/systemd-30D475?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/OpenSearch-005EB8?style=flat-square&logo=opensearch&logoColor=white" />
<img src="https://img.shields.io/badge/Linear-5E6AD2?style=flat-square&logo=linear&logoColor=white" />
<img src="https://img.shields.io/badge/MCP-servers-7c3aed?style=flat-square" />

</div>

<br/>

## 🔁 How my dev loop works

<table>
<tr>
<td width="50%" valign="top">

### Six guarantees, each enforced

| # | Guarantee | Mechanism |
|:-:|---|---|
| 1 | Dev work commits on the dev server, **through gates** | typecheck · API-drift · sweep contract. Fail = no commit, error posted to the issue. Edits are refused until an issue is claimed. |
| 2 | The dev server **can never push** to GitHub | No token, no credential helper, no `gh`. `git push` denied in settings. |
| 3 | Server → laptop **only when I ask** | No cron, no watcher, no timer. By construction. |
| 4 | Laptop → GitHub on **one dev branch** | Branch hardcoded in the publisher. Commits on `main` / `master` / `staging` refused server-side. |
| 5 | The owner merges **when I say** | `main` is read-only to the whole system. |
| 6 | **No credentials ever reach GitHub** | A content-scanning guard aborts on JWTs, live keys, tokens, private keys. Filtered one-commit publish; full history stays home. |

</td>
<td width="50%" valign="top">

### The loop

```text
laptop   open the right workspace
agent    claim an issue        -> edits unlock
         build -> run -> observe  screenshots, curls
         commit through gates  -> fail blocks + logs
me       publish from laptop   -> guard first, read back
         deploy                -> pull-based, /health must answer
         say when to merge     -> main stays the owner's
```

### When it goes wrong

- 🔴 **Gates fail** → no commit, rework label, error as a comment, top of the queue
- 🔴 **Wrong branch** → refused before anything is staged
- 🔴 **Secret found** → push aborts before the fetch. Never withheld. Removed.
- 🟡 **Work left on the floor** → stop hook names the uncommitted files

</td>
</tr>
</table>

<br/>

## 📜 What the agent is told

<div align="center">

| 🏗️ Build, do not describe | ⚡ Decide and do | 🚫 Never fake it |
|:---:|:---:|:---:|
| A write-up is not a deliverable unless docs were asked for | Pick, proceed, report. Stop only for a missing secret or an irreversible action | "Done" means it ran and was observed passing. If it was not run, say so |

| 🎯 Answer the question asked | 🧪 Dev is not production | 💻 Nothing hosted on the laptop |
|:---:|:---:|:---:|
| A scoped request does not become an audit | Publishing is a deliberate act by a person | I work from several machines. Anything bound to one is invisible to the rest |

</div>

<br/>

## 🖥️ How I treat servers

```text
Live beats notes        confirm the host, check its identity, stop if it does not match
Report what you ran     every claim is "ran it", "read it", or UNVERIFIED
Stay in scope           touch only the hosts named in the request
Read-only by default    backup -> rollback written -> one change -> validate -> observe -> log
Keep your own access    never restart SSH or the VPN on the box you are on
Never bind 0.0.0.0      loopback or the private network only
Secrets stay out        names and paths, never values
```

<br/>

## 🚀 Featured work

<div align="center">

<a href="https://github.com/mdrobeulislam1251-ux/T-Ex-LLM-Runpack">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=mdrobeulislam1251-ux&repo=T-Ex-LLM-Runpack&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="T-Ex LLM Runpack" />
</a>
<a href="https://github.com/mdrobeulislam1251-ux/T-Ex-LLM---Agent">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=mdrobeulislam1251-ux&repo=T-Ex-LLM---Agent&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="T-Ex LLM Agent" />
</a>
<a href="https://github.com/mdrobeulislam1251-ux/datryxen-claude">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=mdrobeulislam1251-ux&repo=datryxen-claude&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="datryxen-claude" />
</a>

</div>

**In private, same style:** a B2B lead-data platform with a five-workspace dev pipeline (web, API, MCP, Expo, KMP), a contact-search dashboard over tens of millions of records, scraper orchestration, and a self-hosted n8n stack.

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
