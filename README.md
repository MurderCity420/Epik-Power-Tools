# Epik Power Tools

A Tampermonkey userscript that adds power-user features to [EpikChat](https://epikchat.com).

This is the **development** repo (source of truth). Two release repos are built from it:

| Repo | Who it's for |
|---|---|
| [`Epik-Power-Tools`](https://github.com/MurderCity420/Epik-Power-Tools) | everyone — the public download |
| [`Epik-Power-Tools-Admin`](https://github.com/MurderCity420/Epik-Power-Tools-Admin) | developer-only, includes the Admin tab |

## Install

Install [Tampermonkey](https://www.tampermonkey.net/), then open
[Epik-Power-Tools.user.js](https://raw.githubusercontent.com/MurderCity420/Epik-Power-Tools/main/Epik-Power-Tools.user.js)
and confirm the install prompt. Reload EpikChat — a **blue shield** appears on the right of
the nav bar. Click it to open the panel.

## Features

### Alerts

Know when someone is talking to you.

- **Mention highlighting** — five styles (Subtle, Strong highlight, Bold, Box, Pixie dust)
- **Colours** — use the sender's own chat colour, or pick 1–6 custom colours (2+ cycles
  them for a rainbow effect), with a transparency slider
- **Chime** — 15 built-in alert sounds with a preview button
- **Tab flash** — flashes the browser tab title when you're mentioned while away
- **Reply alerts** — fires when someone quotes or replies to one of your messages
- **Extra keywords** — get pinged on nicknames and variations of your name, not just your
  login

Works identically in both the **Compact** and **Comfortable** chat layouts.

See [docs/alerts.md](docs/alerts.md) for the details.

### Features

- **GIF pop-up** — cap inline GIFs at 70px so they stop swallowing the chat, and open them
  full size in an overlay instead of a new tab.

- **Cams position** — a Top / Left / Right dropdown in EpikChat own Settings -> Layout, so
  the live-stream area can sit beside the chat instead of above it. Scroll and Stack keep
  working and adapt: side-on, Scroll scrolls vertically and Stack wraps into a second column.

- **Collapsible sidebar** — an edge handle that slides the sidebar away and back.

- **Chat header display** — a 4th option in EpikChat's own Settings → Layout. **Compact**
  turns the room tabs into Chrome-style rectangles showing icon + room name, moves the
  description to a hover tooltip, and pulls the room buttons up onto the tab row, removing
  the separate header strip entirely.

- **User list gender filter** — three small toggles at the top of the room list (male,
  female, not specified). Turn one off to hide those users. The room's Online count moves
  up into the room header to make space, and goes back when you turn the feature off.
  Choose which genders are shown by default at login.

See [docs/features.md](docs/features.md) for the details.

## Development

```bash
npm install       # once
npm run build     # build both variants, then auto-push dev + pre-prod
npm run build:only # build only, no git
npm test          # build (no push) + jsdom harness + publish-safety guards
```

### Release stages

| Repo | Stage | Pushed by |
|---|---|---|
| `Epik-Power-Tools-Full` | dev | `npm run build`, automatically |
| `Epik-Power-Tools-Admin` | pre-prod | `npm run build`, automatically |
| `Epik-Power-Tools` | **production** | **by hand, when a release is ready** |

Production is never pushed automatically. The publisher refuses it by repo name *and* by
git remote, and aborts any commit whose staged files contain a session token or JWT.

Edit files in `src/` — never the built output. Bump `@version` in `src/00-header.js` on
every change or Tampermonkey won't auto-update.

See [CLAUDE.md](CLAUDE.md) for the architecture, the EpikChat DOM contract, and the
conventions this codebase follows.

### Layout of this repo

```
src/            the userscript, split into numbered modules
build-obfuscated.js
test/           jsdom harness that runs the built script against real captured markup
docs/           user-facing documentation (mirrored into the release repos)
examples/       captured EpikChat page markup, used as the DOM reference
tasks/          todo.md, lessons.md
```

> `examples/` holds real captures of the site. **Scrub `"token":"..."` from any new
> capture before committing** — it is a live session credential.
