# Slide Readability Review

Reviewed on 2026-11-09. Scope: all 14 main slides and 23 backups in `ivml-cost-benefit.html`, including every reveal step and both themes.

Changes:

- Shortened main slides 5, 7, 10, and 11 while retaining the numerical assumptions and comparison limits.
- Replaced crowded backups 13-15 with larger equations, concise definitions, and aligned explanatory notes.
- Replaced backup 19's crowded chart and duplicate steps with a three-step protocol.
- Shortened repeated workflow keys and added descriptions to the eight editable backup diagrams.
- Removed the 18px workflow-label override, enlarged backups 16-18's diagrams, and adjusted other SVG labels to avoid crowding.
- Repaired 12 malformed diagram outline attributes.
- Fixed backup 20's clipped bottom text by moving full citations into reference notes and keeping short figure captions.

Selected text reductions (headings, equation tokens, and footers included):

| Slide | Before | After |
| --- | ---: | ---: |
| Backup 14: training and re-alignment | 208 | 111 |
| Backup 15: benefit pathways | 192 | 134 |
| Backup 19: applying the framework | 142 | 76 |
| Backup 20: feedback loops | 123 | 75 |

Verification:

- Headless Chrome rendered all 63 slide/reveal states in light and dark mode at 1600 x 900 and 1280 x 720: 252 states checked, with no detected text outside the slide canvas or talk-body/footer overflow.
- Inspected rendered overview sheets in both themes and full-size views of the changed technical layouts and comparison slide.
- Computed contrast checks found no native HTML/SVG slide text below 4.5:1 in either theme. This uses the conservative normal-text threshold from [W3C's contrast guidance](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html).
- All slide images loaded. Figure enlargement and zoom, reveal reversal, navigation limits, and all 37 overview previews passed checks.
- Slide IDs, reveal cues, speaker notes, and the 600-second main-talk budget remain intact. Edited slide text uses ASCII. `git diff --check` passes.

Fine labels inside the original raster paper figures are not covered by the computed text checks. Their large takeaway text and existing "Enlarge figure" controls remain available; use enlargement when discussing fine figure detail. The review follows [W3C's presentation guidance](https://www.w3.org/WAI/teach-advocate/accessible-presentations/), but does not establish complete WCAG conformance or visibility under a particular projector and room setup.


The later main-slide design pass focuses on helping distracted listeners recover the thread. The [visual preview](main-slides-preview.png) shows the completed builds of all 14 main slides.

- Repeated Change / Count / Decide icons connect the overview, active section footer, and closing recap.
- A single workflow spine makes the learning insertion and feedback paths visible without comparing two separate diagrams.
- Correct / Steer / Inspect glyphs identify the three intervention targets. The MitoVis image, large results, update costs, and break-even amounts provide local anchors.
- Consistent headline sizes, spacing, restrained color, and editable SVG drawings replace dense prose panels. Numerical assumptions remain beside the examples that depend on them.
- Main-slide visible text fell from 1,235 to 830 whitespace-separated tokens (about 33 percent), including headings, footers, labels, and equations. Spoken notes total 942 words, leaving about 129 seconds within the 10-minute budget at 120 words per minute for reveals, pointing, and pauses.
- Reviewed the notes at each reveal. All 40 main slide/reveal states were rendered in both themes at both resolutions: 160 states checked with no detected text outside the canvas or viewport, or talk-body/footer overflow. Final native HTML/SVG contrast checks found no values below 4.5:1 and no ordinary text below 20 rendered pixels at 1600 x 900.
- The 23 backup sections and embedded image data remain byte-for-byte identical to their versions before this main-slide pass. Reveal cues match reveal groups, all 37 overview previews remain available, and main navigation still stops at the closing slide.
