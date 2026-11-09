# vis-2026
Presentation initialized by Yixuan W.

Open [ivml-cost-benefit.html](ivml-cost-benefit.html) directly in a browser. The presentation is self-contained: no server, build step, or network is needed.

The [slide readability review](accessibility-review.md) records text reductions, diagram fixes, and verification across both themes and presentation/laptop resolutions. The [main-slide visual preview](main-slides-preview.png) shows every completed main slide.

The main talk follows the contribution in the [highlighted abstract](HighlightedAbstract.pdf): extend Van Wijk's economic model with machine learning, distinguish three interaction targets, and use measurable costs and benefits to decide where interaction is worthwhile. MitoVis supplies the detailed example. A fixed-model audit shows how understanding can create value through failure prevention. The comparison with credible alternatives retains the central concern in Ross's [round-one feedback](round1-feedback.txt).

There are 14 main slides, 23 backups, and 951 words of spoken main-talk notes, excluding references and reveal cues. Per-slide budgets total **10:00**. At 120 words per minute, the notes take about 7:56, leaving about 125 seconds for reveals, pointing, and pauses. This is a pacing estimate; rehearse the diagrams and numerical examples against the slide targets.

- Left/Right or Space advances reveals and slides, stopping at slide 14.
- **G** opens the overview. Section links above the previews jump to backup topics; each backup repeats its topic in the header.
- **Return to the talk** restores the last main slide.
- **P** opens synchronized presenter notes with slide targets and cumulative finish times.
- **N** toggles notes, **F** toggles fullscreen, and the theme control switches light/dark mode.

| Slide | Message | Target | Finish by |
| --- | --- | --- | --- |
| 1 | Cost-Benefit Modeling of IVML Systems | 20s | 0:20 |
| 2 | Useful compared with what? | 30s | 0:50 |
| 3 | Three questions guide the decision | 35s | 1:25 |
| 4 | Learning changes the loop | 50s | 2:15 |
| 5 | Correct. Steer. Inspect. | 50s | 3:05 |
| 6 | From correction to better predictions | 50s | 3:55 |
| 7 | Count effort. Value outcomes. | 50s | 4:45 |
| 8 | Every update has a human cost | 50s | 5:35 |
| 9 | What must one accuracy point be worth? | 70s | 6:45 |
| 10 | Covering costs is only the first test | 50s | 7:35 |
| 11 | Understanding can prevent costly failures | 45s | 8:20 |
| 12 | Stop when the next interaction adds no net value | 45s | 9:05 |
| 13 | Measure what could change the decision | 35s | 9:40 |
| 14 | Thank you - paper and contact links | 20s | 10:00 |

Main slides use a recurring visual shorthand: **Change / Count / Decide**, with matching icons in the contribution overview, section footer, and closing recap. Large result and threshold numbers anchor the worked examples; explanatory detail stays in the notes.

Slide 2 makes the human learning and adaptation burden explicit: **Build. Learn. Use. Adapt.** Its opening notes distinguish learning the interface from interpreting changed model outputs and recovering context after update delays. Paper Sec. 4.1 explicitly models re-alignment; it does not separately parameterize an initial interface-learning curve.

Slide 3 introduces the framework before the worked example: identify the intervention, account for value and effort, and decide whether and when to interact. Slides 4-5 explain the extension to Van Wijk and the three targets: improve data, revise the model or training specification, and understand a fixed model. The main workflow diagram simplifies the paper's notation for progressive explanation; the full workflow and equations remain in backup.

Slides 6-8 place MitoVis's label correction and retraining within that framework. The ledger connects analyst time, interaction frequency, training latency, model improvement, downstream operational savings, and failure-prevention value. The update slide explains how training, review, and resuming work accumulate over repeated updates. Acceptable latency depends on the expected gain and the other costs. The paper does not validate a universal numerical latency bound; the reported 23-second MitoVis update is an example, not a recommended limit.

Slides 9-10 distinguish two break-even questions. The paper's illustrative MitoVis scenario needs about **$889 per percentage point** of accuracy improvement to cover costs against its manual reference. The separate comparison with hypothetical alternative A needs **$1,020 per percentage point** for V to match A. A is introduced for the talk and has no measured head-to-head result. Detailed arithmetic and reuse projections remain in backup 01.

Slide 11 uses the paper's fixed-model audit to connect insight to avoided failures. Slide 12 explains marginal stopping with a schematic of diminishing benefit and rising cost. The original stopping-time curves and their assumptions remain in backup; their numerical crossings are sensitivity results, not observed or recommended session lengths. Slide 13 separates measurements from assumptions and identifies evidence that could change the decision. The closing recap returns to the framework's decisions and retains Rolando's job-market line, email, homepage, and clickable QR links to the [public paper PDF](https://vader.lab.asu.edu/docs/publications/pdf/2026/IVML_paper.pdf) and [LinkedIn profile](https://www.linkedin.com/in/rogarcia-sanz).

Citations and detailed qualifications appear in `notes-reference` paragraphs, available through **N** or **P** and excluded from spoken-word counts and next-slide previews. Essential assumptions stay beside their values. Speaker notes follow the visible text and figures at each reveal; workflow details and numbers are explained on the slide that displays them.

The evidence boundary is explicit throughout. Source: [IVML_Cost_Benefit_2026_VIS.pdf](IVML_Cost_Benefit_2026_VIS.pdf), especially Sections 4, 5.1, and 6. The following inputs have different evidential status:

| Quantity | Value or definition | Status |
| --- | --- | --- |
| Manual vs. MitoVis workflow time | 191.4 vs. 19.0 minutes | Measurements reported in the source study, as summarized in the paper. |
| Neurite-wise classification accuracy | 77.0% -> 87.1%, across three iterations | Reported classifier result; separate from segmentation-mask quality. |
| Initial processing / fine-tuning | 32 seconds / 23 seconds per update | Reported processing times. |
| Analysis workload | Three 19-minute sessions | Paper's illustrative aggregation, not an observed three-session experiment. |
| Expert time / GPU price | $2/minute / $3/hour | Assumed economic proxies. |
| Reorientation | 1.5 minutes per update | Assumed overhead requiring empirical calibration. |
| V: development / runtime | $10,000 / $123.08 | Paper's illustrative development proxy and runtime calculation. |
| Avoided manual-work credit | $1,148.40 per aggregated workload | Paper's scaled manual-effort reference; runtime is subtracted separately. |
| A: development / runtime / classifier gain | $8,000 / $83.08 / 8.1 percentage points | Invented teaching inputs for an ML-assisted editor. No measured head-to-head result. |
| Comparative adoption costs | Learning, integration, and maintenance differences | Need measurement; additional differences are assumed zero in the worked arithmetic. |
| Sustained use and recurring gains | Continued use, workload count, costs, outcomes | Need longitudinal evidence; no adoption claim is made. |

The fixed-model audit uses a normalized 19-minute session at $2/minute and a $10,000 development proxy. With full failure identification and prevention, its $10,038 cost requires an avoided loss of at least $10,038. Lower knowledge acquisition or prevention probability raises the required loss. The normalized duration and full-prevention assumption are illustrative, not measured financial outcomes. Initial training falls outside this fixed-model session's accounting boundary.

Alternative A uses an image editor and a separate training script. A concrete implementation could use [napari's editable label layers](https://napari.org/stable/howtos/layers/labels.html): start with model predictions, correct labels, save them, fine-tune the classifier separately, and reload its predictions. This is ML-assisted because corrected labels feed learning. The comparison asks whether MitoVis's [visual guides and integrated correction/update loop](https://ieeevis.b-cdn.net/vis_2022/posters/v-vis-posters-1021-summary.pdf) justify their additional cost. Implementing and testing A, including the integration work, would be necessary to establish an empirical advantage.

The [2021 MitoVis preprint](https://arxiv.org/pdf/2109.01351), Secs. 3.2 and 5, describes a manual ImageJ-and-Excel reference. The [published journal abstract](https://pure.korea.ac.kr/en/publications/mitovis-a-unified-visual-analytics-system-for-end-to-end-neuronal/) reports up to 13.3 times faster analysis against a conventional manual workflow. A prior source check did not obtain the full journal text, so additional algorithm comparisons or ablations remain unverified. The preprint and journal article are different versions; keep their reported results separate.

Both A and V receive the same $1,148.40 avoided-manual-work credit and use the same value U per percentage point of downstream classifier improvement. Count model utility beyond benefits already credited to the corrected outputs. With other incremental costs assumed zero:

- Net V = $1,148.40 + 10.1U - $10,123.08.
- Net A = $1,148.40 + 8.1U - $8,083.08.
- V covers its modeled costs at U = ($10,123.08 - $1,148.40) / 10.1, or about $889/point.
- At U = $1,000/point, V returns $1,125.32 and A returns $1,165.32: V covers its costs but trails A by $40.
- V's additional net value is 2U - $2,040. The choice reverses at U = $1,020/point. At U = $1,500/point, V leads by $960.

The comparative threshold ranks A and V; manual work remains another option. Use a defensible value range. A range spanning the threshold leaves that comparison unresolved. Paper Sec. 6 supports using relevant model terms, available measurements, literature baselines, logs, and sensitivity ranges. The framework complements empirical evaluation; it does not validate the model's predictive accuracy. Prioritizing measurements that could change the choice is the talk's inference from the framework. Budget evidence gathering separately from adopting and using a workflow.

Backup 01 also gives the reuse threshold: ($2,000/N + $40) / 2, or $1,020, $120, and $30 per point for 1, 10, and 100 independent workloads. This assumes the extra $40 running cost and two-point gain recur on each workload, with no added learning or maintenance cost. Each workload must separately realize its benefit; repeatedly using one improved model does not create another accuracy gain. Reuse projections require longitudinal evidence.

The 23 backups are grouped under six section headers in Grid. The section links stay above the scrolling previews. Main slides use IDs 1-14 and backups retain IDs 15-37.

| Backups | Section | Detail |
| --- | --- | --- |
| 01-02 | Comparison and valuation | Comparison assumptions, arithmetic, reuse, and the value of insight. |
| 03-05 | Worked examples and stopping | Original MitoVis break-even, fixed-model failure-prevention, and stopping-time figures. |
| 06-11 | Workflow and interaction targets | Full workflow, Van Wijk's foundation, and data, model, and understanding targets. |
| 12-15 | Cost-benefit equations | Total model, cost decomposition, training, re-alignment, and benefit pathways. |
| 16-20 | Applying the framework | Application by interaction target, variable mapping, and feedback-loop value. |
| 21-23 | Assumptions and calculations | Inputs behind the paper's thresholds and stopping times. |

Each backup's `data-backup-section` supplies its Grid grouping and presenter label. Keep the matching header aligned when editing. The original paper figures retain their figure numbers and axis details. The fixed-model audit is a different application of the framework, not an alternative solution to MitoVis's task.

Supporting text uses near-black in light mode and near-white in dark mode. Supporting labels, captions, assumptions, and footers use at least 30 slide pixels on the 1600 x 900 canvas; main body copy uses 32 pixels. Editable SVG labels account for diagram scaling, and equation subscripts have a 26-pixel minimum before display fitting. The rendered ordinary HTML/SVG text floor is 28 pixels at a 1600 x 900 viewport. Original paper images retain their embedded labels and enlargement controls. Preserve hierarchy through size and weight rather than low-contrast gray. Embedded image assets and offline behavior are preserved. Main/backup counts and presenter timing derive from slide metadata. Keep visible content, assumptions, and each slide's speaker-notes template together, with reference paragraphs separate from spoken notes and reveal cues.
