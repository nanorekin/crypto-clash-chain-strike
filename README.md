# Crypto Clash: Chain Strike

A free, single-file browser fighting game. Land hits to build a chain, fill the meter and fire a Chain Strike. No build step, no backend, no fees.

## Play

- **Arcade ladder:** four opponents with rising difficulty, ending with the Genesis boss.
- **Quick fight:** pick your fighter, your opponent and the difficulty.
- **2 players:** local versus on one keyboard.

### Controls

| Action | One player | Player 1 (2P) | Player 2 (2P) |
| --- | --- | --- | --- |
| Move | A / D or arrows | A / D | Left / Right |
| Jump | W or Up | W | Up |
| Block | S or Down (or walk backwards under attack) | S | Down |
| Punch | J or Z | F | , |
| Kick | K or X | G | . |
| Chain Strike | L or C | H | / |
| Pause | Esc or P | | |

On phones and tablets, on-screen buttons appear under the arena (in landscape they float over the bottom corners).

### Moves and combos

- **Dash:** double-tap left or right.
- **Uppercut:** hold Block, then press Punch. It launches the enemy.
- **Sweep:** hold Block, then press Kick. A low hit that jumpers avoid.
- **Chain Strike (full meter):** each fighter has their own: Block Reward, Double Confirm, Tidal Slam, Fast Forward, Genesis Burst.
- **Named combos** (land the three hits in order inside one chain for bonus damage and meter): Hash Rush (Punch, Punch, Kick), Fork Lift (Punch, Kick, Uppercut), Ledger Sweep (Kick, Kick, Sweep), Mempool Mix (Kick, Punch, Punch).

### Daily challenge

A new challenge every day at 00:00 UTC: a fixed opponent, arena, difficulty and rule twist, the same for everyone. Win one fight to clear it and keep your daily streak. Everything is stored in the player's browser.

### Fighters

Nine fighters, each with a passive ability and their own Chain Strike: Hash Miner, Validator, Whale, Relay, Hodler, Rug Puller, Oracle, MEV Bot and the supporter-only Genesis. Everyone has about 30% more health than the base stats, so fights last a bit longer.

### Music

Original dark techno / industrial tracks, synthesised live in the browser with the Web Audio API (no audio files). A slower menu theme, a driving fight theme that changes key per arena, and extra intensity when someone is low on health. The Music and Sfx buttons at the top toggle them separately; the choice is remembered.

### Easier options

Casual difficulty for the arcade ladder and quick fights, and a Training mode where the dummy never fights back and your Chain Strike refills.

## Deploy on GitHub Pages

1. Create a new repository, for example `crypto-clash-chain-strike`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/crypto-clash-chain-strike/`.

## Donations

The tip card at the bottom of the page works the same way as in Feeless Defence:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter perks (Genesis fighter and Gold Vault arena) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

Note: the supporter unlock is stored in the player's browser (`localStorage`), so it is a thank-you perk, not secure access control.

## Files

- `index.html`: the whole game, styles and scripts.
- `README.md`: this file.

Add `?selftest` to the URL to expose a small `window.__cc` object for automated tests.
