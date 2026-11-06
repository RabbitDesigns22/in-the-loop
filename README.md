# in-the-loop

**Many agents, one shared picture of what is happening now.**

`in-the-loop` is an agent skill for Claude Code (and any agent that reads `SKILL.md` skills). When several chats or agents work for the same person, each one only sees its own conversation: one deploys a new version while another keeps reviewing the old one, one changes a setting and another changes it back, and the user has to repeat the news to everyone. `in-the-loop` gives them a shared live board: every agent reads it before acting and writes one line after any change others should know. They stay informed without stepping into each other's work.

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

## License

MIT. Made by [Rabbit Designs](https://github.com/RabbitDesigns22).
