# Personal fork

This plugin is maintained in https://github.com/relsett/herdr-auto-title.
Upstream: https://github.com/kryptamine/herdr-auto-title.

## Local behavior

`HERDR_AUTO_TITLE_TITLE_ONLY=true` shows the thread title without repository,
branch, agent name or tab position. Only a Codex terminal title loses its known
` | directory` suffix; real agent titles and transcript topics are preserved.
Outer quotation marks are removed. Manual tab names are still protected.
The setting is off by default.

## Installation and maintenance

Install this fork, not upstream:

```sh
herdr plugin install relsett/herdr-auto-title --ref main
```

The existing plugin ID `herdr.auto-title` keeps the same local configuration.
Personal settings remain in `~/.config/herdr-auto-title/config.env`; they are
not shipped in this repository. Herdr records the installed source and commit
in `herdr plugin list`.

Develop on a feature branch, fetch upstream separately, and review its changes
before merging them. Run `make check` before publishing. Push tested changes to
this fork's main branch, reinstall from it, and check live tab names. Restart
only this plugin when applying an update; do not stop Herdr or its agents.
