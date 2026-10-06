# SpaceTris

A free falling-block puzzle game where every piece is a refractive crystal. The nebula behind the board bends and shimmers through the glass, line clears shatter into shards, and two optional sci-fi rulesets add power cores and cascade gravity on top of the classic rules.

**Play it in your browser:** https://nbwillcox.github.io/SpaceTris/

Everything is generated in code: the nebulae, the glass blocks and all sound effects and music (Web Audio synthesis). There are no image or audio files and no build step. A sibling of [SpaceBobble](https://github.com/nbwillcox/SpaceBobble), [SpaceHarrier](https://github.com/nbwillcox/SpaceHarrier), [SpaceContra](https://github.com/nbwillcox/SpaceContra) and the rest of the Space series.

## Controls

| Action | Keyboard | Gamepad | Touch |
| --- | --- | --- | --- |
| Move | `←` `→` (hold to slide) | d-pad / left stick | ◀ ▶ buttons |
| Soft drop | `↓` | d-pad down | ▼ button |
| Hard drop | `↑` or `Space` | d-pad up / right trigger | DROP button |
| Rotate left / right | `A` / `D` (also `Z` / `X`) | `X`,`B`,`LB` / `A`,`RB` | ⟲ ⟳ buttons |
| Hold | `S`, `Shift` or `C` | `Y` / left trigger | HOLD button |
| Pause / restart | `P` or `Esc` / `R` | `Start` | |

The key delay (DAS) and repeat rate (ARR) are adjustable in Settings. Touch buttons appear automatically on touch devices.

## Modes

- **Marathon:** endless classic play; the level (and the nebula sector behind the board) changes every 10 lines.
- **Sprint 40:** clear 40 lines as fast as you can.
- **Ultra 2:00:** two minutes, highest score wins.
- **Versus CPU:** a garbage battle against one of four named opponents (Scout Drone, Rogue Pirate, Station Cmdr, The Overmind).

Rules follow the modern guideline: SRS rotation with wall kicks, 7-bag, hold, ghost piece, lock delay with move reset, T-spins (full and mini), back-to-back bonuses, combos and perfect clears.

## Sci-fi rulesets (Marathon, Sprint and Ultra)

- **Power cores:** some pieces arrive with a glowing core cell. When its line clears it fires: **BOMB** (3x3 blast), **LASER** (clears its whole column), **FREEZE** (gravity nearly stops for 8 seconds) or **NOVA** (clears the rows above and below). Cores caught in a blast fire too, so they chain.
- **Cascade gravity:** after every clear, all loose glass shards drop individually to the floor. That can complete new lines, which chain for a growing bonus.

High scores are kept separately for every mode and ruleset.

## Run locally

It is plain HTML/CSS/JS. Either open `index.html` directly, or serve the folder:

```bash
python -m http.server 8000
```

then visit http://localhost:8000. Handy URL parameters: `?play=marathon` (or `sprint`, `ultra`, `versus`) skips the menu, with `&cores=1`, `&cascade=1`, `&level=N` and `&opp=0-3`.

## License and attribution

Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): free to play, share and remix **non-commercially**, as long as you give credit and **link back to this repository**: https://github.com/nbwillcox/SpaceTris

This is an original game inspired by classic falling-block puzzle games. It uses no assets, names or code from any existing game.
