# Features

Optional extras that change how the EpikChat page itself behaves.

## Chat header display

This one lives in **EpikChat's own settings** — the gear icon in the nav bar, then
**Layout**. Power Tools adds a fourth option there, below "chat message display".

| Option | What you get |
|---|---|
| **Comfortable** | The site's normal look: a row of round room icons, then a separate strip below it with the room name, a divider, the room description, and the room buttons. |
| **Compact** | Everything folds into one row. |

In **Compact**:

- Room tabs become rectangular, Chrome-style, each showing its icon (shrunk to 20px)
  with the room name beside it — so you can tell rooms apart without hovering.
- The room description becomes a **tooltip**: hover any tab to read it, not just the one
  you are in. EpikChat only tells the page the current room's description, so each one is
  remembered the first time you visit that room and kept for next time. A room you have
  never opened shows its name until you do.
- The divider is gone, and the room buttons (share, favourite, member count, leave) move
  up onto the tab row.
- The separate header strip disappears entirely, giving that vertical space back to chat.

Your choice is remembered per account.

## GIF pop-up

EpikChat has a **gif images** switch in its own **Settings -> Chat**. Power Tools adds a
**pop-up images** toggle directly below it, and it is useful whichever way that switch is
set:

| gif images | With pop-up images on |
|---|---|
| **Off** | The "Click to view GIF" link opens the GIF in a pop-up over the chat instead of a new tab. |
| **On** | The GIF still shows in chat but is capped at **70px tall**, on its own line under the sender name, so it no longer pushes the conversation off screen. Click it to see it full size in the same pop-up. |

Close the pop-up with the X, by clicking anywhere outside the image, or with Escape.

## Column sides

EpikChat puts the user list on the left and the sidebar on the right. Two dropdowns in the
site own **Settings -> Layout** let you swap either one:

- **user list position** - Left or Right
- **sidebar position** - Left or Right

### Combining them

Put **both on the same side** and they share one column. The user list becomes a fourth
tab in the sidebar tab strip - a cam icon, first in the row, selected by default. Click
Home / Friends / Media to switch the column to the sidebar, and the cam tab to switch it
back.

While combined, the sidebar collapse handle is hidden - it collapses the sidebar only,
which is now just the top half of a shared column, so it had nothing sensible to do.
Separate the two again and it comes back.

The shared column keeps the **user list width** whichever tab is showing, so switching
between them does not resize the column.

The tab strip is sized to 40px to match the nav bar, with the four tabs sharing the width
evenly. If you have turned EpikChat own sidebar off, there is no tab strip to share, so
the two stay as separate columns.

## Cams position

EpikChat always puts the live-stream area above the chat. Power Tools adds a **Top /
Left / Right** dropdown to the site own **Settings -> Layout -> live stream display**,
just under its Scroll and Stack radios.

| Position | Result |
|---|---|
| **Top** | The site normal layout, unchanged. |
| **Left** | Cams in a column to the left of the chat, below the room tabs. |
| **Right** | The same, on the right. |

The room-tab bar keeps the full width in every position — only the chat area shares the
row with the cams.

The site existing **Scroll** and **Stack** choice still applies, and reads naturally in
each position:

| | Scroll | Stack |
|---|---|---|
| **Top** | one row, scrolling sideways | wraps onto a second **row** |
| **Left / Right** | one column, scrolling up and down | wraps into a second **column** |

The column sizes itself to whichever cam size is in use (small or large) and never takes
more than half the window.

### Rearranging cams

EpikChat lets you drag a cam to reorder it, but it sets that up for its own single-row
layout — so in **Stack**, or in the Left/Right positions, a cam could only be dragged
along one axis and never moved between rows or columns. Power Tools unlocks the drag
whenever the layout needs it, so a cam can be dropped anywhere in the grid. Plain
**Top + Scroll** is genuinely a single row, so it is left exactly as the site had it.

### Moving a cam to a second row or column

Cams pack themselves: on top they fill across the row, on the left or right they fill down
the column, and they wrap to a new line when the current one is full. Because cams come in
different sizes, a line holds however many happen to fit — two large ones, or three small
ones — which is what lets you build an arrangement like:

    [  large  ][  large  ]
    [small][small][small]
    [  large  ][  large  ]

To start a new line **early**, drag a cam past the end of the current one — below the strip
when the cams are on top, out to the side when they're on the left or right. A dashed strip
shows where to drop. That cam moves to the start of a new line and stays there; drag others
onto the line to join it.

Drag it back into an earlier line to undo it. Nothing else is affected: the packing, the
fill direction and the wrapping are all exactly as they were.

If a cam you moved out disappears — they turned their cam off — its line closes on its own.

## Collapsible sidebar

The sidebar (trending rooms, friends, media) gains a small handle on its inner edge.
Click the double arrows to slide it out of the way and give the width to chat; click again
to bring it back. Your choice is remembered per account.

This is separate from EpikChat's own **Settings → Layout → sidebar** switch, which removes
the sidebar entirely — this keeps it one click away.

---

## User list gender filter

Turn it on in EpikChat's own **Settings → Layout → gender filter**, alongside the site's
other layout options — there is nothing to configure in the Power Tools panel.

It adds three small circular toggles to the top of the room's user list:

| Button | Shows |
|---|---|
| ♂ blue | Male |
| ♀ pink | Female |
| ? grey | Unknown — users who didn't specify a gender |

Click one to hide everyone of that gender from the list; click it again to bring them
back. A toggled-off button is dimmed.

The toggles sit where the room's **"N Online"** count used to be. That count isn't lost —
it's shown up in the room header instead, just left of the Share button, and keeps
updating as people come and go. Turn the feature off and it returns to its original spot.

Users whose row carries no gender badge at all are treated as **not specified**, so they
follow that toggle rather than becoming permanently unhideable.

### Defaults at login

The toggles reset every time you sign in. The **Male / Female / Unknown** checkboxes that
appear under the switch in **Settings → Chat** decide what they reset *to* — so if you
always want female users hidden, untick **Female** and it will be off in every session.
They are only shown while the filter is switched on.

Clicking a toggle in the user list only affects the current session; it never rewrites
your default.

### Notes

- Hiding a gender only affects **your** view of the list. Nobody else sees any change,
  and hidden users can still message you.
- Filtered users are never drawn in the first place, so the list doesn't flicker or jump
  when it refreshes or when you change rooms.
- The filter cooperates with the site's own user-list search box — using both at once
  works as you'd expect.
- The Online count keeps showing the **room's** total, not the number of rows currently
  visible after filtering.
- **The Viewers list is never filtered.** While you are broadcasting, the Room / Viewers
  switch swaps the same list between room users and the people watching your cam. The
  gender toggles apply only to the room list — switch to Viewers and you always see
  everyone, whatever the toggles are set to. They keep their state, so switching back
  to Room restores your filtering.
