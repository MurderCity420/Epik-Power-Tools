# Epik Power Tools

A Tampermonkey userscript that adds power-user features to [EpikChat](https://epikchat.com).


## Quick start

1. **[Install Tampermonkey + the script →](docs/installation.md)**
2. Reload your EpikChat tab.
3. Click the blue **shield** icon at the right of the nav bar to open the panel.

➡️ **[Install / Update Epik Power Tools](https://raw.githubusercontent.com/MurderCity420/Epik-Power-Tools/main/Epik-Power-Tools.user.js)** (requires Tampermonkey — see the [installation guide](docs/installation.md) first)

## Features

### Alerts

Know when someone is talking to you.

- **Mention highlighting** — five styles (Subtle, Strong highlight, Bold, Box, Pixie dust)
- **Colours** — use the sender's own chat colour, or pick 1–6 custom colours (2+ cycles
  them for a rainbow effect), with a transparency slider
- **Chime** — 15 built-in alert sounds with a preview button
- **Tab flash** — flashes the browser tab title when you're mentioned while away
- **Reply alerts** — fires when someone quotes or replies to one of your messages
- **Viewer alerts** — a notification when someone starts watching your cam
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

## Documentation

- **[Installation](docs/installation.md)** — install Tampermonkey and the script
- **[Alerts](docs/alerts.md)** — mentions, replies, viewer alerts, chimes and highlighting
- **[Features](docs/features.md)** — layout controls, GIF pop-up, gender filter

## Browser compatibility

Tested on Chrome, Edge and Firefox with Tampermonkey. Any Chromium browser that runs
Tampermonkey should work.

