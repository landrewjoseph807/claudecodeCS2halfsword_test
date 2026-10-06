# Brief for the coding agent (Claude Code / Codex) with Melty access

Goal: finish, test and publish this CS2 mashup on Melty as a draft. Read README.md and sheets/ first. Do not put any token in this repo.

Rules from the project owner
- CS2 is the host. Half Sword Demo is not in Melty's catalog: it is role "secondary" at most, and only its combat rules are used (no assets, no look-alikes of its content).
- Single player plus bots. No recipe.multiplayer.
- Ask before building anything that loads into CS2. Keep it offline / `-insecure`; never work around VAC.
- The owner wants no further questions: pick sensible defaults, record them in the README.

Steps
1. Connect to Melty. Call game_info for counter-strike-2, search_mashups, mashup_info on the closest existing one.
2. Verify each row in sheets/hooks.json (status "unverified") against CS2's real modding route (workshop tools / addon Lua vscripts). Set status to "verified" only after it works in the running game. If melee, hit-zone damage or bot control cannot be done, report that plainly and cut scope.
3. Implement from generated/loadout_data.lua (run tools/gen_lua.py after any sheet change; change sheets before code).
4. Run tools/preflight.py until clean. Test on Dust 2 with 1 human + 9 bots.
5. Run inspect_package, validate_recipe, one_click_check. If one-click is impossible, say what players would have to install by hand.
6. Capture a real screenshot of the mod running. Choose a license, then create_mod as a draft, upload, add_screenshot, submit_release, save melty.json at the repo root. Publish only after the owner approves.
