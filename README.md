# vis-2026
Presentation initialized by Yixuan W.

Open [ivml-cost-benefit.html](ivml-cost-benefit.html) directly in a browser. The presentation is self-contained: no server, build step, or network is needed.

The revised talk responds to Ross's [round-one feedback](round1-feedback.txt) by following a skeptical stakeholder choosing between workflows for neuronal mitochondria analysis. Its central question is: **What additional value does a proposed visualization create over credible alternatives, and when is that value worth its additional cost?**

There are 14 main slides, 23 backups, and 1,306 words of main-talk speaker notes. The current draft targets 12:00 for a ten-minute slot; it includes expanded transition explanations and still needs trimming. At 120 words per minute, the notes take about 10:53, leaving roughly 70 seconds for pointing and pauses within the draft target. Rehearse against the per-slide targets, particularly the comparison and threshold slides. The opening overview allows 60 seconds; the returns allow 50 and 55 seconds to explain how the preceding section leads to the next.

- Left/Right or Space navigates the talk and stops at slide 14.
- **G** opens the overview: the main talk comes first, followed by backups.
- Choose backups for questions; **Return to the talk** restores the last main slide.
- **P** opens synchronized presenter notes with slide targets and cumulative finish times.
- **N** toggles notes, **F** toggles fullscreen, and the theme control switches light/dark mode.

| Slide | Message | Target | Finish by |
| --- | --- | --- | --- |
| 1 | Cost-Benefit Modeling of IVML Systems | 25s | 0:25 |
| 2 | Useful compared with what? | 35s | 1:00 |
| 3 | Overview - Compare workflows | 60s | 2:00 |
| 4 | Which workflow should the lab invest in? | 55s | 2:55 |
| 5 | Compare workflows on the same task. | 45s | 3:40 |
| 6 | Return to overview - Model value | 50s | 4:30 |
| 7 | Every workflow needs the same cost-benefit ledger. | 60s | 5:30 |
| 8 | Model updates also consume expert attention. | 45s | 6:15 |
| 9 | Covering its costs does not make it the best choice. | 70s | 7:25 |
| 10 | How much must the extra improvement be worth? | 85s | 8:50 |
| 11 | Repeated use can change the decision. | 50s | 9:40 |
| 12 | Return to overview - Test the contribution | 55s | 10:35 |
| 13 | What evidence would make the contribution convincing? | 50s | 11:25 |
| 14 | Make the value of a new workflow explicit. | 35s | 12:00 |

Slide 1 foregrounds the full paper title, with the stakeholder question as a subtitle. After the evaluation problem, slide 3 asks **"When is a new visualization worth using?"** It follows one lab's choice of tools through three questions: what the tool adds over alternatives, whether the improvement is worth the time and money, and what still needs measuring. The same questions return on slides 6 and 12, marking completed sections and highlighting the next one. The overview notes follow the visible questions in order and explain why each leads to the next. Slide 6 moves from comparing tools to weighing the improvement against its cost; slide 12 connects those two questions to the evidence still needed. Workflow details and numerical examples are discussed on the slides that display them. Where space allows, content-slide footers track these sections and underline the current one. Slide 4 omits the progress footer to give the example more room. The closing recap follows the same sequence.

Slide 4 introduces the lab director's decision and three workflows: manual work, a proposed image editor with a separate training script (A), and the MitoVis workflow (V). Slide 5 (originally slide 4) defines a fair comparison with shared conditions on the left and stacked A/V workflow lanes on the right, replacing the three equal cards. Slides 7-8 build the ledger from that decision, including expert reorientation after model updates. Slides 9-11 work through explicitly hypothetical costs and outcomes for A, a value threshold, and reuse. Slide 13 states the evidence needed to evaluate the contribution. The closing thank-you slide includes Rolando's faculty-job-market line. The title-slide definition is in the spoken introduction; source footers identify sources and assumptions.

The evidence boundary is explicit throughout. Source: [IVML_Cost_Benefit_2026_VIS.pdf](IVML_Cost_Benefit_2026_VIS.pdf), especially Sections 4 and 5.1. The following inputs have different evidential status:

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

A is a proposed workflow using a scientific image editor and a separate training script. A concrete implementation could use [napari, a viewer and editor for scientific images](https://napari.org/stable/howtos/layers/labels.html), with editable label layers over microscopy images for correcting boundaries and relabeling regions. Start with the same predictions as V, inspect and edit masks and neurite labels in the editor, save corrected neurite labels, run a separate script to fine-tune the same classifier, then load its new predictions. The editor can also support manual annotation; A is ML-assisted because the model supplies initial annotations and learns from the corrections. The comparison asks whether MitoVis's [visual guides suggesting similar neurites to inspect and integrated correction/update loop](https://ieeevis.b-cdn.net/vis_2022/posters/v-vis-posters-1021-summary.pdf) justify their additional cost. Connecting the editor's corrected labels to the classifier requires integration work that must be measured. A's costs and outcomes remain invented teaching inputs. A real recommendation requires implementing this comparator and benchmarking it alongside the strongest relevant alternatives on the same task. Hold the starting model and training recipe fixed to help separate the visual workflow's contribution from the learner's contribution.

A is introduced for this talk; our cost-benefit paper does not evaluate it. The [2021 MitoVis preprint](https://arxiv.org/pdf/2109.01351), Secs. 3.2 and 5, describes a manual ImageJ-and-Excel reference. The [published journal abstract](https://pure.korea.ac.kr/en/publications/mitovis-a-unified-visual-analytics-system-for-end-to-end-neuronal/) reports up to 13.3 times faster analysis against a conventional manual workflow. The full journal text was inaccessible during this check, so additional algorithm comparisons or ablations remain unverified. The preprint and journal article are different versions; keep their reported results separate.

Slide 9 rounds dollars for readability and adds a V - A column so the extra cost and improvement are visible. Exact values remain in backup 01 and below. Both A and V receive the same $1,148.40 avoided-manual-work credit and use the same value U per percentage point of downstream classifier improvement. Count model utility beyond the corrected outputs so the same outcome is not credited twice. With all other incremental costs assumed zero:

- Net V = $1,148.40 + 10.1U - $10,123.08.
- Net A = $1,148.40 + 8.1U - $8,083.08.
- At U = $1,000/point, V returns $1,125.32 and A returns $1,165.32: V pays off against manual work but trails A by $40.
- V's additional net value is 2U - $2,040. The choice reverses at U = $1,020/point. At U = $1,500/point, V leads by $960.

Slide 10 uses an editable SVG with linear axes to show this crossing. Its "A ahead" and "V ahead" regions rank those two workflows; manual work remains another option, especially when both modeled net values are negative. It asks the stakeholder for a defensible range, rather than requiring an exact valuation. A range crossing the threshold leaves the choice unresolved. For insight without a defensible monetary value, connect knowledge to a decision or avoided loss, retain uncertainty, or compare effort to a defined knowledge outcome.

Slide 11 spreads the hypothetical additional $2,000 development cost across N independent workloads. Assuming the extra $40 runtime cost and 2-point gain recur on each workload, the threshold becomes ($2,000/N + $40) / 2: $1,020 at N=1, $120 at N=10, and $30 at N=100. The formula is retained in backup 01; the main slide emphasizes the thresholds and assumptions. These projections assume no additional learning or maintenance cost. Each workload must separately realize its benefit; repeatedly using one improved model does not automatically generate a new accuracy gain. Reuse projections do not establish lasting impact.

The 23 backups contain:

- 01-02: comparison assumptions/arithmetic and the challenge of valuing insight.
- 03-06: the paper's MitoVis break-even curve, fixed-model failure-prevention case, stopping-time analysis, and unified workflow figure.
- 07-23: the original 17 technical backups, including taxonomy, equations, benefit pathways, application tables, and supporting calculations.

The original MitoVis threshold of about $889 per point remains in backup 03 with its manual reference. It answers a different question from the main talk's $1,020 comparative threshold. The fixed-model audit's $10,038 threshold and the stopping-time curves also remain conditional worked examples. Neither ranks alternative solutions to the MitoVis task.

Embedded image assets and offline presentation behavior are preserved. Slide IDs are consecutive; main/backup counts and presenter timing derive from slide metadata. Keep visible content, source assumptions, and each slide's speaker-notes template together when editing.
