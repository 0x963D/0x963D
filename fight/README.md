# Profile animation

Run `python fight/make_fight.py` from the repository root to regenerate both
themes. `python fight/make_fight.py --check` verifies that the committed assets
match the generator. Install `fight/requirements.txt` and either Arial on Windows
or Liberation Sans on Linux before rebuilding.

The four lines in `PARAS` are an introduction adapted from the profile bio. The
full bio remains in the root README. Keep `things` at six characters because the
original kick has six individual letter trajectories. The other word targets
are `video.`, `shaders,`, `APIs,`, and `production.`. Update their lookups if the
copy changes.

The 31-second fight, poses, effects, and palettes come from the supplied
[source revision](https://github.com/bulletchicken/bulletchicken/blob/d412291fb8b52f9440755e513dafc623af56362f/fight/make_fight.py).
Local changes are the profile copy and word targets, Windows font lookup,
deterministic clip identifiers, output paths, a rebuild check, and a static
introduction for reduced-motion preferences. The README selects separate still
assets because motion preferences inside an SVG image are not reliable in every
browser context. The animation does not load scripts,
external images, fonts, or services. The profile has no visible attribution line.
