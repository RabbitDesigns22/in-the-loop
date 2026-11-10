# in-the-loop

**Many agents, one shared picture of what is happening now.**

`in-the-loop` is an agent skill for Claude Code (and any agent that reads `SKILL.md` skills). When several chats or agents work for the same person, each one only sees its own conversation: one deploys a new version while another keeps reviewing the old one, one changes a setting and another changes it back, and the user has to repeat the news to everyone. `in-the-loop` gives them a shared live board: every agent reads it before acting and writes one line after any change others should know. They stay informed without stepping into each other's work.

## See the difference

> **You:** (Session B, an hour after session A moved a webhook)

**Without the skill:** session B reviews the old webhook, reports it as broken and "fixes" it back.

**With the skill:** session B reads the shared board first, sees one line from A (time, what changed, how it was confirmed) and leaves A's work alone.

**Skip it if** you only ever run one session at a time.

**Status:** in daily use in the author's own setup. Plain instructions, no scripts, no network calls. MIT. Issues and suggestions welcome.

## Install

With the [skills CLI](https://skills.sh):

```bash
npx skills add RabbitDesigns22/in-the-loop
```

Or manually: copy `skills/in-the-loop/` into `~/.claude/skills/` for all your projects, or into `.claude/skills/` for one project.

To make every session use it, add this line to your `CLAUDE.md` (with your own path):

```
At the start of every task and before reviewing, deploying or changing anything shared, load the in-the-loop skill and read /path/to/LIVE.md.
```

## Works well with

- [`report-now`](https://github.com/RabbitDesigns22/report-now): reports of right now, not of yesterday.
- [`sort-me-out`](https://github.com/RabbitDesigns22/sort-me-out): one ordered list of everything pending and forgotten.
- [`hands-on`](https://github.com/RabbitDesigns22/hands-on): the agent does every step it can.

## Español

**Que todos los chats estén al tanto.** Cuando varios chats trabajan para la misma persona, cada uno solo ve su conversación: uno sube una versión nueva y otro sigue revisando la vieja, uno cambia algo y otro lo regresa. `in-the-loop` les da un tablero en vivo compartido: cada chat lo lee antes de actuar y escribe una línea después de cualquier cambio que los demás deban saber (versión subida, ajuste cambiado, decisión, en qué está trabajando el usuario ahora). Saben lo que pasa sin meterse en el trabajo del otro.

Instalar: `npx skills add RabbitDesigns22/in-the-loop`

## More skills from the same setup

These come from one real workflow: a small agency run with 15+ Claude Code sessions in parallel. Each skill fixes one problem that kept happening there.

| Skill | What it fixes |
|---|---|
| [one-pass](https://github.com/RabbitDesigns22/one-pass) | get it right the first time; stop paying tokens for rework |
| [hora-exacta](https://github.com/RabbitDesigns22/hora-exacta) | real date and time in every message, so nothing lands on the wrong day |
| [hands-on](https://github.com/RabbitDesigns22/hands-on) | the agent does what it can and only asks you for codes, keys and payments |
| [easy-for-them](https://github.com/RabbitDesigns22/easy-for-them) | steps people actually follow: direct link, one action per line |
| [one-answer](https://github.com/RabbitDesigns22/one-answer) | one thought-through answer instead of plan, fix, new plan |
| [never-twice](https://github.com/RabbitDesigns22/never-twice) | a shared error log so no session repeats a known mistake |
| [report-now](https://github.com/RabbitDesigns22/report-now) | status checked live this minute, stamped with the time |
| [sort-me-out](https://github.com/RabbitDesigns22/sort-me-out) | one ordered list of what is urgent, waiting and forgotten |
| [study-first](https://github.com/RabbitDesigns22/study-first) | reads everything in full and answers point by point, no invented details |
| [session-watchdog](https://github.com/RabbitDesigns22/session-watchdog) | wakes the sessions that got stuck mid-task, leaves the rest alone |
| [skill-harvest](https://github.com/RabbitDesigns22/skill-harvest) | reads your sessions and finds the skills you are missing |
| [small-budget-ads](https://github.com/RabbitDesigns22/small-budget-ads) | Meta Ads rules for 1-5 USD a day ad sets |
| [whatsapp-closer](https://github.com/RabbitDesigns22/whatsapp-closer) | evidence-ranked rules for a WhatsApp sales assistant that closes |
| [whatsapp-number-onboarding](https://github.com/RabbitDesigns22/whatsapp-number-onboarding) | connect a number to the WhatsApp Cloud API in the safe order |
| [proposal-pdf](https://github.com/RabbitDesigns22/proposal-pdf) | short PDF proposals with every price checked against its source |
| [published-vs-planned](https://github.com/RabbitDesigns22/published-vs-planned) | says "published" only for what it saw live on the public page, Facebook and Instagram checked apart |
| [source-every-fact](https://github.com/RabbitDesigns22/source-every-fact) | every price, phone and name on a post traced to its source, nothing added |
| [only-what-was-asked](https://github.com/RabbitDesigns22/only-what-was-asked) | "pause only Google Ads" pauses only Google Ads, and proves the rest did not move |
| [model-per-chat](https://github.com/RabbitDesigns22/model-per-chat) | the right model for each chat: top model where mistakes cost money, cheap or none where it only runs often |

If one of them saved you a redo, a star helps other people find it.

## License

MIT. Made by [Rabbit Designs](https://github.com/RabbitDesigns22).
