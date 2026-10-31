# Profile fight verification

Verified animation/source commit:
[`85a57f1`](https://github.com/0x963D/0x963D/tree/85a57f1552435e6393c9ea5e43c7ad0ebabb92ed).
The original profile wording is from
[`c713113`](https://github.com/0x963D/0x963D/blob/c7131138373ff58aeea55916254a30097f5dd1f5/README.md).

![Before and after, captured in GitHub](before-after.png)

[Watch the full animation loop](fight-preview.mp4).

The heading, introduction, and all five bullets now use the existing wording
verbatim, with no extra greeting, summary, emoji, or duplicated bio. The generator
reads that content from `fight/profile.md`. Working principles and current tools
remain unchanged native Markdown below the image.

Checks performed on October 31, 2026:

- Compared `fight/profile.md` with the original Git revision, ignoring trailing
  blank lines only. The content matches.
- Reconstructed the text in both static SVGs and compared it with the source
  introduction. The words and punctuation match, in order.
- Checked the generated README remainder against the original source. It matches
  and does not repeat the introduction.
- `python fight/make_fight.py --check` passes for all four SVGs and the README.
- SVGs parse successfully, have unique IDs, and resolve their clip references.
- The immutable GitHub README loads its matching SVG assets. Both reduced-motion
  variants select still files and produce identical screenshots over time.
- Inspected the introduction, chase, and reset; recorded a complete loop from
  the matching local SVG. Normal animation loads without a script or external
  asset dependency.
- At 390px, GitHub has no document-wide horizontal overflow. The fixed-width
  SVG scales down like the reference, so its text is small on phones. The full
  introduction is also present in the image's alt text. The existing principles
  code block scrolls horizontally on narrow screens.

This PR remains draft pending visual acceptance. No merge or live-profile change
has occurred. The task checkout is retained for corrections until that decision.
