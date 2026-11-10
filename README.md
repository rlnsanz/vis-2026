# vis-2026

IEEE VIS 2026 talk: **Cost-Benefit Modeling of IVML Systems**. Presentation initialized by Yixuan W.

## Open the deck

Open [ivml-cost-benefit.html](ivml-cost-benefit.html) in a browser. It is self-contained: no server, build step, or network needed.

- **Left/Right** or **Space**: next/previous reveal or slide
- **G**: overview grid, with links to backup sections
- **P**: presenter view with notes and timing
- **N**: toggle notes, **F**: fullscreen; the theme control switches light/dark

## The talk

The argument: extend Van Wijk's economic model of visualization to machine learning, distinguish three interaction targets (data, model, understanding), and use measurable costs and benefits to decide where interaction is worthwhile. MitoVis is the worked example.

12 main slides, 10-minute limit. Slide budgets total 8:40; the script (~1,130 words) reads in about 9:26 at 120 wpm. These are estimates, not rehearsal times.

| Slide | Message | Target |
| --- | --- | --- |
| 1 | Cost-Benefit Modeling of IVML Systems | 20s |
| 2 | Useful compared with what? | 30s |
| 3 | Put interaction where it creates value (and then stop) | 35s |
| 4 | Learning changes the loop | 50s |
| 5 | What you change shapes the cost and payoff | 50s |
| 6 | Correct what you see. Retrain the model. | 50s |
| 7 | Count the costs. Put a number on the value. | 50s |
| 8 | Every update has a human cost | 50s |
| 9 | What must one accuracy point be worth? | 70s |
| 10 | Covering costs is only the first test | 50s |
| 11 | Stop when the next interaction adds no net value | 45s |
| 12 | Thank you - paper and contact links | 20s |

## Key numbers and what backs them

- **$889 per accuracy point**: what MitoVis (V) needs to cover its costs against the manual workflow.
- **$1,020 per accuracy point**: what V needs to match alternative A (image editor + separate training script).
- **Measured** (source study): 191.4 vs. 19.0 min workflow time; 77.0% -> 87.1% classifier accuracy; 23 s per update.
- **Assumed**: $2/min expert time, $3/h GPU, 1.5 min reorientation per update, $10,000 development proxy.
- **Invented for the talk**: all of alternative A's inputs. There is no measured head-to-head result.

Full arithmetic and assumptions are in backups 01 and 21-23.

## Backups

23 backups, grouped into six sections in the overview grid.

| Backups | Section |
| --- | --- |
| 01-02 | Comparison and valuation |
| 03-05 | Worked examples and stopping |
| 06-11 | Workflow and interaction targets |
| 12-15 | Cost-benefit equations |
| 16-20 | Applying the framework |
| 21-23 | Assumptions and calculations |

## Files

- [IVML_Cost_Benefit_2026_VIS.pdf](IVML_Cost_Benefit_2026_VIS.pdf) - the paper (mainly Secs. 4, 5.1, 6)
- [HighlightedAbstract.pdf](HighlightedAbstract.pdf) - the contribution the talk follows
- [round1-feedback.txt](round1-feedback.txt) - Ross's round-one feedback
- [accessibility-review.md](accessibility-review.md) - readability and contrast review
- [main-slides-preview.png](main-slides-preview.png) - all main slides at a glance
- [AGENTS.md](AGENTS.md) - conventions for editing slides and speaker notes

## Editing tips

- Colors follow the [IEEE VIS 2026 palette](https://ieeevis.org/year/2026/welcome/): orange `#df6824`, raspberry `#bb4a72`, brown `#693a19`, cream `#f3dfcf`.
- Keep slide text at 30 px or larger on the 1600 x 900 canvas (body copy 32 px).
- Each backup's `data-backup-section` sets its grid group; keep it in sync with the slide header.
- Speaker notes should follow what is on screen at each reveal step (see [AGENTS.md](AGENTS.md)).
