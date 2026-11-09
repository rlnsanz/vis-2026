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
- Correct / Steer / Understand glyphs identify the three intervention targets. The MitoVis image, large results, update costs, and break-even amounts provide local anchors.
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

Projection typography pass on 2026-11-09:

- Enlarged supporting labels, captions, assumptions, counters, and footers to at least 30 slide pixels across all 14 main slides and 23 backups. Main body copy uses 32 pixels; equation subscripts and superscripts have a 26-pixel minimum before display fitting.
- Enlarged editable SVG text with diagram scaling taken into account. Widened title-diagram labels, split "Human effort" across two lines, and moved repeated workflow annotations to clear nodes and arrows. Shortened redundant diagram labels without changing the interaction pathways.
- Rendered all 63 slide/reveal states in both themes at 1600 x 900 and 1280 x 720: 252 states checked, with no detected canvas overflow or talk-body/footer overflow. Ordinary native HTML/SVG text measures at least 28 rendered pixels at 1600 x 900 and 22.4 at 1280 x 720; mathematical subscripts and superscripts are checked separately from this ordinary-text floor.
- Inspected the completed deck overview and full-size title, chart, equation, table, and workflow layouts. An independent visual check confirmed the workflow-label fixes in both themes.
- Speaker notes, reveal metadata, timing targets, presentation scripts, and embedded images remain byte-for-byte unchanged. Main navigation still stops at slide 14, reveal reversal works, and all 37 Grid previews remain available. No JavaScript exceptions were detected. Edited text uses ASCII, and `git diff --check` passes.
- Refreshed `main-slides-preview.png`. Fine text embedded in original paper figures and interface screenshots is outside the native-text size checks; the paper figures retain their enlargement controls and large accompanying explanations.

Title-figure balance adjustment on 2026-11-09:

- Gave Data, Model, and Understanding equal 320 x 76 target boxes. Centered Data above the human-effort hub and mirrored the lower pair and their connectors around its centerline.
- Expanded the SVG viewBox and used uniform 40-unit labels, preserving the figure's displayed height. Labels render at about 30.5 pixels at 1600 x 900 and 24.4 at 1280 x 720, with space around the longest label.
- Inspected both themes at both resolutions: no clipping, label collisions, or slide overflow. Speaker notes still match the figure's human-effort and intervention-target content. Refreshed `main-slides-preview.png`; slide content outside this figure and its text-size rule is unchanged.

Understanding-target refinement on 2026-11-09:

- Renamed slide 5 to "Correct. Steer. Understand." The understanding card now covers learning or relearning model behavior and names comparison as part of the effort.
- Aligned the notes with each reveal. The final reveal explains version comparison, including A/B testing, and how data or model changes can require revised expectations. Studying a fixed model still adds no retraining.
- Checked slide 5's three reveal states in both themes at 1600 x 900 and 1280 x 720: 12 states, with no detected text outside the slide or viewport, body overflow, footer overlap, or JavaScript exceptions. Inspected the completed slide in both themes.
- Refreshed `main-slides-preview.png` from all 14 current completed slides and synchronized README labels and pacing. Slide 5 has 83 spoken words within its 50-second target; main-talk notes total 968 words, about 8:04 at 120 words per minute, leaving about 116 seconds for reveals and pauses. The total target remains 600 seconds. Edited text uses ASCII; `git diff --check` passes.

Effort and value clarification on 2026-11-09:

- The data card names correcting labels, cleaning data, and improving features. Its potential value is clearer relationships and the possibility that simpler models suffice. The notes use simple regression as an explanatory example.
- The model card names fitting and tuning models, diagnosing errors, and validation. Its notes explain repeated runs, validation on held-out data, computing resources per run, and analyst time to interpret results. Its value is meeting accuracy, latency, and resource targets. A shared footer accounts for training and review costs across intervention targets when required.
- The third card labels its target "Human knowledge" and its action "Understand." Its effort is "understand what changed and why" and its value is "deeper mastery; faster iteration." Notes explain how A/B comparisons can make the next experiment faster to run.
- Notes follow each reveal: data improvements and regression, model-fitting effort and requirements, then mastery, iteration, and shared costs. They retain relearning, A/B comparison, the fixed-model distinction, and the reference note about counting overlapping benefits once.
- Checked all 12 slide 5 states across both themes at 1600 x 900 and 1280 x 720. The final wording fits without detected slide overflow, body overflow, footer overlap, or JavaScript exceptions; completed slides were inspected in both themes. Refreshed the main-slide preview.
- Slide 5 has 84 spoken words within its 50-second target. Main-talk notes total 969 words, about 8:05 at 120 words per minute, leaving about 115 seconds within the unchanged 600-second budget. README labels and pacing are synchronized; edited text uses ASCII and `git diff --check` passes.

Read-aloud speaker-script pass on 2026-11-09:

- Reviewed all 110 spoken paragraphs across the 14 main slides and 23 backups. Rewrote 86 paragraphs on 33 slides; retained passages already suitable to read aloud.
- Replaced outline fragments, detached instructions, and compressed accounting phrases with connected spoken explanations. Preserved the accepted data, model-fitting, mastery, and iteration framing, along with reported quantities and their qualifications.
- Wrote currency, decimals, and mathematical labels as spoken wording. Kept explanations beside their visible figures and reveal steps. Slide 4 now connects view exploration to human understanding before introducing the three intervention targets.
- Moved the pronunciation cue out of spoken prose. Preserved all original reference paragraphs and click cues; added separate reference-only notes for the pronunciation aid and contextual details that are not needed in the current spoken passage.
- Corrected the presenter's next-slide preview to exclude click instructions as well as references. Checked rendered notes and cue states at all 63 slide/reveal states in both the presentation and presenter views: 126 states, with no JavaScript exceptions or mismatches. Inspected the presenter view with the revised slide 5 script.
- Main-talk script totals 1,030 words, about 8:35 at 120 words per minute, leaving about 85 seconds within the unchanged 600-second target. Each main slide retains time for pauses within its existing budget. This is a pacing estimate, not a timed rehearsal.
- Slide content, figures, styles, embedded assets, reveal metadata, and timing targets are unchanged. The only presentation-code change filters click cues out of the next-slide script preview. The visual preview remains current. Edited spoken text uses ASCII, and `git diff --check` passes.

VIS 2026 palette update on 2026-11-09:

- Matched the conference site's orange `#df6824`, raspberry `#bb4a72`, brown `#693a19`, and cream `#f3dfcf`, using its [official stylesheet](https://ieeevis.org/year/2026/_astro/DefaultLayout.vvxjtq71.css). Added darker text shades, warm light surfaces, and pale accents on dark brown surfaces for dark mode.
- Applied the palette to all editable slides and diagrams, the overview, speaker-note cues, and presenter controls. Costs use raspberry; benefits use brown. Original embedded figures and their corresponding legend swatches retain their source colors.
- Checked all 63 slide/reveal states in both themes at 1600 x 900 and 1280 x 720: 252 states and 5,348 native HTML/SVG text checks. No sampled text contrast below 4.5:1, canvas overflow, missing slide images, or JavaScript exceptions were detected. Contrast checks use a conservative background tint for the main-slide gradients; text embedded in raster figures is outside this check.
- Inspected title, target, ledger, chart, backup-diagram, overview, and presenter views. Refreshed `main-slides-preview.png` from the 14 completed main slides.
- Confirmed forward and reverse reveals, the slide-14 navigation stop, all 37 overview previews, and the 600-second target. Slide text, speaker notes, layout markup, navigation code, image data, and the vendor runtime are unchanged by this palette pass. All 14 Decide icons retain their thin dashed vertical guide.

Stronger VIS color use on 2026-11-09:

- Replaced pale takeaway panels with saturated orange, raspberry, and brown bands. Raspberry now carries more headings, primary accents, backup labels, and presenter controls. Colored header strips and borders make the intervention cards and effort/value ledger more distinct.
- Filled the title diagram's equal-sized boxes with orange for Data, raspberry for Model, and brown for Understanding. Split the connectors into three matching colors and retained a neutral human-effort hub. The intervention cards repeat these target colors. White text on raspberry and brown, and dark text on orange, keep the filled labels readable in both themes.
- Rendered all 252 slide/reveal/theme/viewport combinations again. All 5,348 sampled native HTML/SVG text checks passed 4.5:1 contrast, with no detected canvas overflow, missing slide images, or JavaScript exceptions. Inspected the completed title in both themes and the intervention cards and ledger at full size.
- Refreshed the main-slide preview. Speaker notes, slide text, timing targets, navigation code, image data, and the vendor runtime are unchanged; the title diagram's paths were split only to color the three existing connectors independently. All 14 dashed Decide guides remain intact.

Metric-unit spacing on 2026-11-09:

- Removed the large numerals' inherited negative letter spacing from `min` on slide 6 and `s` on slide 8. Both metrics now use normal unit lettering, baseline alignment, and an explicit 12-slide-pixel gap between the number and its unit.
- Checked all 32 affected reveal/theme/viewport combinations, with no detected text contrast failures, canvas overflow, missing images, or JavaScript exceptions. Inspected slide 6 and refreshed the main-slide preview. Speaker notes and metric values are unchanged.

Title-slide simplification on 2026-11-09:

- Removed the title diagram and its unused styles. Expanded the title to two 84-pixel lines, retaining the visible decision question, authors, affiliations, and logos.
- Aligned the opening note with the title and decision question instead of the removed intervention-target figure. The title slide has 35 spoken words within its unchanged 20-second target; the full main-talk script now has 1,031 words.
- Checked the title slide in both themes at 1600 x 900 and 1280 x 720, with no detected contrast failures, canvas overflow, missing images, or JavaScript exceptions. Inspected both themes and refreshed the main-slide preview. All other slide content, notes, reveal metadata, and timing targets are unchanged.
