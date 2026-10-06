# Dust 2 Half Sword (CS2 mode)

Status: DESIGN AND DATA ONLY. Not built, not tested, not published. No gameplay code exists yet.

An offline Counter-Strike 2 mode on Dust 2: 5v5, you plus 9 bots, with a smith's shop instead of the gun buy menu. Armor pieces and heavy weapons cost money and weight. Where a hit lands decides the damage, and carrying weight slows you down. Bots charge the nearest enemy and swing.

## How Half Sword is in it
Through its combat rules only (slow committed swings, hit-zone damage, armor coverage, weight). CS2 and Half Sword are different engines, so no Half Sword assets are used or shipped.

## Safety
Offline or private server started with `-insecure`. Never run this on VAC-secured servers. Single player with bots only; no multiplayer.

## Layout
- `sheets/` source of truth: weapons, armor, hit_zones, bot_loadouts, rules, hooks
- `tools/preflight.py` checks unfilled cells, broken references, bot budgets
- `tools/gen_lua.py` turns the sheets into `generated/loadout_data.lua`
- `AGENT_BRIEF.md` what remains and how to finish it

## Licensing and credits
No license chosen yet. Add one before publishing.
