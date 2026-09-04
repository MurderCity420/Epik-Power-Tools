# Alerts

The Alerts tab controls what happens when someone talks to you in chat — how the
message is highlighted, whether a sound plays, and whether the room tab flashes.

Open it with the **blue shield** on the right of the EpikChat nav bar (or press
**Ctrl+Shift+E**).

## What counts as a mention

A message alerts you when any of these is true:

- it contains **@yourname**
- it contains **your login name** as a whole word
- it contains one of your **extra mention keywords** as a whole word
- someone **replies to or quotes one of your messages** (if *Alert when replied to* is on)

Your own messages never alert you.

Matching is always **whole-word**, for your name and for every keyword. "audacity" will
not alert someone called "murdrcity", and "@murdrcityfan" is a different person.

If an alert ever surprises you, open **Settings → Log** — every mention records the exact
term that matched, e.g. `Alerts - Mention from snot — matched "murd"`, so you can see which
keyword was responsible and remove it.

**Whole-word matching** means a short nickname like `ag` will match "ag" and "ag!" but
not "again" or "agree". This is what stops a two-letter nickname pinging on half the room.

Quoted text inside a reply is deliberately **not** scanned for your name. A reply quotes
someone else's message — if that quote happens to contain your name, that isn't a new
mention of you. Only the reply's own text counts, plus the fact that it was addressed to
you.

## Highlight style

Five looks for a highlighted message:

| Style | What it does |
|---|---|
| **Subtle** | A coloured left border with a soft gradient fade |
| **Strong highlight** | Fills the whole message row with the colour |
| **Bold text** | Bolds the message and colours the sender's name |
| **Box border** | Draws a coloured box around the message |
| **Pixie dust** | Animated sparkles that twinkle over the sender's name |

## Highlight color

Two sources:

- **Senders color** — uses the colour that person already chats in. Different people get
  different highlights automatically.
- **Custom color** — pick your own. Add up to **6** colours with the **+** button:
  - **1 colour** — every highlight uses it
  - **2–6 colours** — highlights cycle through them, one colour per message. With *Bold*
    the sender's name is rainbowed letter-by-letter; with *Pixie dust* the sparkles take
    turns through the list.

The **Transparency** slider controls how see-through the highlight is. Higher percentage =
more see-through. It affects all five styles, not just the filled ones.

> Very dark chat colours (a lot of EpikChat users pick near-black) are automatically
> lightened until they're readable against the chat background. Your chosen hue is kept —
> only the brightness moves.

## Alert behavior

- **Chime when mentioned** — plays a sound. Pick from 15 built-in chimes with the
  dropdown, and preview any of them with the **▶** button. All are synthesized in the
  browser; nothing is downloaded.
- **Flash the room tab** — the chat tab the mention arrived in blinks until you open it,
  so you can see at a glance which room or IM wants you. It also flashes the *browser* tab
  title while EpikChat is in the background, since an in-page blink can't be seen once
  you've switched to another window; that part stops as soon as you come back.
- **Alert when replied to** — treats someone quoting or replying to your message as a
  mention. On by default.

> EpikChat already shows its own notification for **pokes**, so Power Tools deliberately
> stays out of the way there.

### When alerts fire

An alert fires **once, the moment the message arrives** — whichever tab you happen to be
looking at. A mention in a room or IM you aren't currently viewing chimes straight away and
flashes that tab.

Switching between tabs never re-triggers anything. Revisiting a conversation re-applies the
highlighting on the messages, but the chime and the flash belong to the message arriving,
not to it being drawn, so an old mention stays quiet no matter how often you come back to
it.

## Viewer alerts

EpikChat tracks who is watching your cam, but never tells you when someone starts — it
just quietly changes the number next to your own preview. This puts a notification in the
site's own bubble stack (top right) the moment someone starts watching.

- **Notify when someone views your cam** — a bubble reading *"**Name** is viewing your
  cam"*, which fades after about ten seconds. On by default.
- **Chime** — its own sound, separate from the mention chime, so you can tell the two
  apart without looking. Defaults to Google Pop. Same 15 chimes and the same **▶**
  preview.
- **Flash the Browser tab** — off by default here. Flashes only while the tab is hidden,
  exactly like the mention version.

**This only works while your cam is on.** EpikChat only sends viewer information about
*your own* stream, so with your cam off there is nothing to report and the feature is
silent. That is a limit of what the site tells the browser, not a bug.

A few details worth knowing:

- **Nobody is announced twice.** If someone stops watching and starts again, that counts
  as a new arrival and you get a second bubble — which is usually what you want.
- **Reloading mid-stream is quiet.** Anyone already watching when the script loads is
  recorded silently, so you don't get a burst of bubbles for viewers you already had.
- **The site's own viewer count keeps working normally.** Power Tools runs after it,
  never instead of it.

> There is no equivalent for *other* people. EpikChat only sends per-user viewer counts
> for the site-wide top 5 in the sidebar, so a "viewers" number beside everyone in the
> user list isn't possible.

## Extra mention keywords

Add nicknames, a shortened first name, or common misspellings of your username. Anything
in this list pings you the same way your real name does.

Type it in the box and press **Add** (or Enter). Remove one with the trash button.

Keywords are stored lowercased and matched case-insensitively.

## Where settings are stored

Settings are saved **per EpikChat account**. If two people share a browser and log into
different accounts, each gets their own settings — nothing bleeds across.

Back them up from **Settings → Data → Download settings**, and restore the file on another
machine with **Restore from file**.
