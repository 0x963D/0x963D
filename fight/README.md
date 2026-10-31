# Profile animation

Run `python fight/make_fight.py` from the repository root to regenerate both
themes. `python fight/make_fight.py --check` verifies that the committed assets
match the generator. Install `fight/requirements.txt` and either Arial on Windows
or Liberation Sans on Linux before rebuilding.

`profile.md` contains the approved profile wording. The generator reads
the heading, introduction, and five bullets from that file and draws them once
inside the animation. Current tools remain native Markdown below it. Dan requested
removal of the working-principles section. The generator also produces the root
README and checks it for copy drift.

The kicked word is `state,`, which has six characters for the six original letter
trajectories. The other targets are `recovery;`, `ownership,`, `architecture`, and
`connected`. Keep the approved wording intact when changing the effect.

The 31-second fight, poses, effects, and palettes come from the supplied
[source revision](https://github.com/bulletchicken/bulletchicken/blob/d412291fb8b52f9440755e513dafc623af56362f/fight/make_fight.py).
Local changes are the verbatim profile layout and word targets, Windows font lookup,
deterministic clip identifiers, output paths, a rebuild check, and a static
introduction for reduced-motion preferences. The README selects separate still
assets because motion preferences inside an SVG image are not reliable in every
browser context. Each theme has its own picture with a motion-only source query;
GitHub's theme fragment controls which image is visible. Combining theme and motion
in a source query fails because GitHub rewrites that entire query for account themes.
The animation does not load scripts,
external images, fonts, or services. The profile has no visible attribution line.
