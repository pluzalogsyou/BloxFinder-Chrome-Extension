# BloxFinder

**Join any Roblox user in-game even with joins turned off.**

Chrome / Edge / Brave / Opera extension. Manifest V3.

The Chrome Web Store listing (`bnpkdbbfehooennlcojneoimfjgekdgn`) is gone. This repo is the source so you can Load unpacked yourself.

Not affiliated with Roblox Corporation.

---

## Features

- **Player finder** — locate the server a user is on and join them, including when they have joins off or have blocked you
- **Clothing export** — one-click download of original shirt / pants / t-shirt templates
- Follows the language of your Roblox account

---

## Install (Load unpacked)

Chrome no longer installs random `.crx` files. Use the folder.

1. Download this repo: **Code → Download ZIP**, or `git clone`
2. Unzip. You need the folder that contains `manifest.json` at the root
3. Open `chrome://extensions` (Edge: `edge://extensions`, Brave: `brave://extensions`)
4. Enable **Developer mode** (top right)
5. **Load unpacked** → select that folder
6. Pin BloxFinder on the toolbar if you want

Leave the folder where it is. Chrome loads from that path. If you move or delete it, the extension dies until you Load unpacked again.

**Update:** pull / download the new zip, overwrite the files in the same folder, click **Reload** on the extensions page.

---

## Find a player

1. Open the Roblox game you think they are in
2. Go to the **Servers** tab
3. Click **BloxFinder**
4. Type their **username**
5. Click **Find** and wait

It scans public server lists. Small games are fast. Huge games take longer and can miss if they are not on a listed server, not in that experience, or the scan times out.

You still have to be able to join that experience (not banned, not private-server-only, etc.).

---

## Export a clothing template

1. Open any **original** Roblox clothing item (shirt, pants, t-shirt)
2. Click **Export Template**
3. The texture is saved to your Downloads folder

Works on catalog items that have a template asset. UGC / layered clothing that does not expose a classic template will not export.

---

## Permissions

| Permission | Why |
|---|---|
| `scripting` | Inject the finder UI and export button on roblox.com |
| `storage` | Save settings |
| `*://*.roblox.com/*` | Run on Roblox pages and call Roblox APIs the site already uses |

That is the full original set. No `cookies`, no `<all_urls>`, no extra hosts.

---

## Repo layout

manifest.json background.js findPlayers.js exportClothing.js _locales/ images/


Exact files may differ by version. `manifest.json` must stay at the **root** of the folder you Load unpacked.

---

## Requirements

- Chrome 120+, Edge, Brave, or another Chromium with MV3
- A Roblox account signed in on roblox.com
- Developer mode for sideload

Chromebook / managed school Chrome often blocks Load unpacked (`chrome://policy`). Use a personal profile.

---

## FAQ

**It does not show up on Roblox**  
Reload the extension, hard-refresh roblox.com (`Ctrl+Shift+R`). Confirm the extension is enabled and not sitting in “Errors”.

**Find never returns**  
Wrong game, user offline, user in a private/reserved server, or the experience has too many servers. Try a smaller game first to confirm the UI works.

**Join lands in a random server**  
The scan can race; retry. Roblox may also refuse a join if the instance is full.

**Developer mode warning every launch**  
Normal for unpacked extensions. Click the warning away. It is not a virus prompt from this source.

**Can I put this back on the Chrome Web Store?**  
Only as a clean MV3 zip with these permissions. Do not add extra hosts or cookie access.

---

## Disclaimer

Third-party tool. Use it in line with [Roblox Terms of Use](https://en.help.roblox.com/hc/en-us/articles/115004647846). Joining people who turned joins off can violate their privacy expectations and Roblox rules. Clothing templates you export are still Roblox / creator IP — do not steal and reupload.

---

## License

Source in this repository. Not an official Roblox product.
