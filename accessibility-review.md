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

Slide 2's learning and adaptation update makes the human effort explicit with "Build. Learn. Use. Adapt." The opening notes explain interface learning, interpretation of changed model outputs, and context recovery after delays, before the alternatives appear. The reference notes distinguish these costs from a separately parameterized learning curve, which the manuscript does not provide.

- Checked all three slide 2 reveal states in both themes at 1600 x 900 and 1280 x 720: 12 states, with no detected text outside the slide or viewport, body overflow, footer overlap, or JavaScript exceptions.
- Compared the notes with the visible material at each reveal and inspected the completed light slide and initial dark slide. Updated the main-slide visual preview.
- Current spoken main-talk notes total 951 words, leaving about 125 seconds at 120 words per minute. Slide 2 retains its 30-second target and the total budget remains 600 seconds. Edited slide text and notes use ASCII; `git diff --check` passes.

Speaker-notes polish on 2026-11-09:

- Polished all 14 main slides and 23 backups for spoken clarity, shorter phrasing, natural pauses, and transitions tied to the current slide.
- Slide 3 now follows Change / Count / Decide before explaining the Van Wijk extension. Each question has its own speaking beat, and the count step explains why the intervention target matters.
- Checked the spoken notes against the visible content at all 40 main slide/reveal states and all 23 static backups. Numerical explanations stay with their supporting figures. Background study details without a local visual anchor remain available in reference-only notes.
- Main-talk notes still total 951 words, excluding reveal cues and references. At 120 words per minute, every main slide fits its existing target with room for pauses and clicks; the full talk leaves about 125 seconds within its 10-minute budget. This is a pacing estimate, not a timed rehearsal.
- All markup outside the speaker-note templates, including visible slides, figures, presentation code, and timing targets, is byte-for-byte unchanged. Original reveal cues and reference paragraphs are preserved. Edited notes use ASCII, and `git diff --check` passes. The visual preview remains current.
