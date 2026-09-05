# Installation

[← Back to README](../README.md)

Epik Power Tools is a **userscript** — it runs inside the Tampermonkey browser extension.
Installing takes about two minutes.

---

## Step 1 — Install Tampermonkey

Click the link for your browser and follow the prompts:

- **[Chrome](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)**
- **[Firefox](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)**
- **[Edge](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd)**

---

## Step 2 — Pin Tampermonkey to your toolbar

Pinning puts the Tampermonkey icon in your toolbar so you can reach it quickly.

- **Chrome / Edge** — Click the puzzle-piece **Extensions** icon (top-right), then click the 📌 pin next to Tampermonkey.
- **Firefox** — Right-click the Tampermonkey icon and choose **Pin to Toolbar**.

| Chrome / Edge | Firefox |
|:---:|:---:|
| ![Pin in Chrome or Edge](screenshots/pin-chrome-edge.png) | ![Pin in Firefox](screenshots/pin-firefox.png) |

---

## Step 3 — Allow user scripts *(Chrome and Edge only — Firefox can skip)*

Chrome and Edge need one extra setting before userscripts will run.

1. Right-click the **Tampermonkey icon** in your toolbar.
2. Click **Manage Extension**.
3. On the extension page, turn on **Allow access to file URLs** and **Allow User Scripts** (the exact wording varies by browser version).

| Step 3a — Manage Extension | Step 3b — Enable the setting |
|:---:|:---:|
| ![Right-click manage extension](screenshots/manage-extension.png) | ![Enable allow user scripts](screenshots/allow-user-scripts.png) |

---

## Step 4 — Install the script

Click the button below. Tampermonkey will open a confirmation page showing the script name,
version, and the sites it runs on.

**➡️ [Install Epik Power Tools](https://raw.githubusercontent.com/MurderCity420/Epik-Power-Tools/main/Epik-Power-Tools.user.js)**

Click **Install** on that page.

---

## Step 5 — Reload EpikChat

Refresh your EpikChat tab. Everything lives in EpikChat's own **Settings** — the gear icon
in the nav bar. You'll find **Chat Alerts** near the top, extra options on the **Layout**
and **Chat** pages, and **EPT Data** / **EPT Logs** at the bottom of the list. You're done!

---

## Updating

Tampermonkey checks for new versions automatically and will prompt you when one is
available. To force a check now, open **EpikChat's own Settings** (the gear icon in the
nav bar) and click **EPT Check** at the top of the panel, beside the close button — it
turns into **EPT Upgrade** when a newer version is waiting. Both labels name the tool, so
there is no mistaking them for an update to EpikChat itself. Tampermonkey's **Check for userscript
updates** menu item does the same thing.

The version you have installed is shown at the bottom of that same Settings panel, on the
line with EpikChat's own version:

```
v4.5.71 · Release Notes | EPT v0.0.65 · Docs
```

**Docs** opens this documentation.

## Uninstalling

Open the Tampermonkey dashboard, find **Epik Power Tools** in the list, and click the
trash icon. Your settings stay in Tampermonkey's storage unless you also clear the
extension's data, so reinstalling brings them back.

---

## Troubleshooting

**No Chat Alerts row in Settings.**
Check the script is enabled in the Tampermonkey dashboard, and that you're on
`epikchat.com`. On Chrome and Edge, re-check Step 3 — this is the first thing that fails
when **Allow User Scripts** is off.

**Settings look right but nothing highlights.**
The chat lives inside a frame that loads a moment after the page. Give it a few seconds
after a reload, then try again.

**Settings vanished after switching accounts.**
That's deliberate — settings are stored **per EpikChat account**, so two people sharing a
browser each get their own. Log back into the original account and they return.

---

**Next:** [Alerts →](alerts.md) · [Features →](features.md)
