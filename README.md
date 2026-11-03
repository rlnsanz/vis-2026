# vis-2026
Presentation initialized by Yixuan W.

Open [ivml-cost-benefit.html](ivml-cost-benefit.html) directly in a browser. The presentation is self-contained: no server, build step, or network is needed.

The revised talk responds to Ross’s [round-one feedback](round1-feedback.txt) by following a skeptical stakeholder choosing between workflows for neuronal mitochondria analysis. Its central question is: **What additional value does a proposed visualization create over credible alternatives, and when is that value worth its additional cost?**

There are 11 main slides, 23 backups, and 936 words of main-talk speaker notes. The pacing target is 9:30 inside a ten-minute slot. At 120 words per minute, the notes take about 7:48, leaving roughly 102 seconds for pointing and pauses. Rehearse against the per-slide targets, particularly the comparison and threshold slides.

- Left/Right or Space navigates the talk and stops at slide 11.
- **G** opens the overview: the main talk comes first, followed by backups.
- Choose backups for questions; **Return to the talk** restores the last main slide.
- **P** opens synchronized presenter notes with slide targets and cumulative finish times.
- **N** toggles notes, **F** toggles fullscreen, and the theme control switches light/dark mode.

| Slide | Message | Target | Finish by |
| --- | --- | --- | --- |
| 1 | Cost-Benefit Modeling of IVML Systems | 25s | 0:25 |
| 2 | Useful compared with what? | 40s | 1:05 |
| 3 | Which workflow should the lab invest in? | 55s | 2:00 |
| 4 | Compare workflows on the same task. | 45s | 2:45 |
| 5 | Every workflow needs the same cost–benefit ledger. | 60s | 3:45 |
| 6 | Model updates also consume expert attention. | 45s | 4:30 |
| 7 | Covering its costs does not make it the best choice. | 70s | 5:40 |
| 8 | How much must the extra improvement be worth? | 85s | 7:05 |
| 9 | Repeated use can change the decision. | 50s | 7:55 |
| 10 | What evidence would make the contribution convincing? | 60s | 8:55 |
| 11 | Make the value of a new workflow explicit. | 35s | 9:30 |

Slide 1 foregrounds the full paper title, with the stakeholder question as a subtitle. Slide 3 introduces the lab director’s decision and three workflows: manual work, a hypothetical ML-assisted alternative (A), and the proposed MitoVis workflow (V). Slide 4 defines a fair comparison. Slides 5–6 build the ledger from that decision, including expert reorientation after model updates. Slides 7–9 work through an explicitly hypothetical alternative, a value threshold, and reuse. Slide 10 states the evidence needed to evaluate the contribution. The closing thank-you slide includes Rolando’s faculty-job-market line. The title-slide definition is in the spoken introduction; visible footers are reserved for sources and assumptions.

The evidence boundary is explicit throughout. Source: [IVML_Cost_Benefit_2026_VIS.pdf](IVML_Cost_Benefit_2026_VIS.pdf), especially Sections 4 and 5.1. The following inputs have different evidential status:

| Quantity | Value or definition | Status |
| --- | --- | --- |
| Manual vs. MitoVis workflow time | 191.4 vs. 19.0 minutes | Measurements reported in the source study, as summarized in the paper. |
| Neurite-wise classification accuracy | 77.0% → 87.1%, across three iterations | Reported classifier result; separate from segmentation-mask quality. |
| Initial processing / fine-tuning | 32 seconds / 23 seconds per update | Reported processing times. |
| Analysis workload | Three 19-minute sessions | Paper’s illustrative aggregation, not an observed three-session experiment. |
| Expert time / GPU price | $2/minute / $3/hour | Assumed economic proxies. |
| Reorientation | 1.5 minutes per update | Assumed overhead requiring empirical calibration. |
| V: development / runtime | $10,000 / $123.08 | Paper’s illustrative development proxy and runtime calculation. |
| Avoided manual-work credit | $1,148.40 per aggregated workload | Paper’s scaled manual-effort reference; runtime is subtracted separately. |
| A: development / runtime / classifier gain | $8,000 / $83.08 / 8.1 percentage points | Invented teaching inputs for an ML-assisted editor. No measured head-to-head result. |
| Comparative adoption costs | Learning, integration, and maintenance differences | Need measurement; additional differences are assumed zero in the worked arithmetic. |
| Sustained use and recurring gains | Continued use, workload count, costs, outcomes | Need longitudinal evidence; no adoption claim is made. |

The hypothetical A workflow uses predictions, conventional editing, and fine-tuning. It specifies a comparison to conduct; it is not presented as an identified, empirically evaluated state-of-the-art competitor. A real recommendation requires choosing the strongest relevant tools and measuring their performance on the same task. Hold the starting model and training recipe fixed to help separate the visual workflow’s contribution from the learner’s contribution.

Slide 7 rounds dollars for readability and adds a V − A column so the extra cost and improvement are visible. Exact values remain in backup 01 and below. Both A and V receive the same $1,148.40 avoided-manual-work credit and use the same value U per percentage point of downstream classifier improvement. Count model utility beyond the corrected outputs so the same outcome is not credited twice. With all other incremental costs assumed zero:

- Net V = $1,148.40 + 10.1U − $10,123.08.
- Net A = $1,148.40 + 8.1U − $8,083.08.
- At U = $1,000/point, V returns $1,125.32 and A returns $1,165.32: V pays off against manual work but trails A by $40.
- V’s additional net value is 2U − $2,040. The choice reverses at U = $1,020/point. At U = $1,500/point, V leads by $960.

Slide 8 uses an editable SVG with linear axes to show this crossing. Its “A ahead” and “V ahead” regions rank those two workflows; manual work remains another option, especially when both modeled net values are negative. It asks the stakeholder for a defensible range, rather than requiring an exact valuation. A range crossing the threshold leaves the choice unresolved. For insight without a defensible monetary value, connect knowledge to a decision or avoided loss, retain uncertainty, or compare effort to a defined knowledge outcome.

Slide 9 spreads the hypothetical additional $2,000 development cost across N independent workloads. Assuming the extra $40 runtime cost and 2-point gain recur on each workload, the threshold becomes ($2,000/N + $40) / 2: $1,020 at N=1, $120 at N=10, and $30 at N=100. The formula is retained in backup 01; the main slide emphasizes the thresholds and assumptions. These projections assume no additional learning or maintenance cost. Each workload must separately realize its benefit; repeatedly using one improved model does not automatically generate a new accuracy gain. Reuse projections do not establish lasting impact.

The 23 backups contain:

- 01–02: comparison assumptions/arithmetic and the challenge of valuing insight.
- 03–06: the paper’s MitoVis break-even curve, fixed-model failure-prevention case, stopping-time analysis, and unified workflow figure.
- 07–23: the original 17 technical backups, including taxonomy, equations, benefit pathways, application tables, and supporting calculations.

The original MitoVis threshold of about $889 per point remains in backup 03 with its manual reference. It answers a different question from the main talk’s $1,020 comparative threshold. The fixed-model audit’s $10,038 threshold and the stopping-time curves also remain conditional worked examples. Neither ranks alternative solutions to the MitoVis task.

Embedded image assets and offline presentation behavior are preserved. Slide IDs are consecutive; main/backup counts and presenter timing derive from slide metadata. Keep visible content, source assumptions, and each slide’s speaker-notes template together when editing.
