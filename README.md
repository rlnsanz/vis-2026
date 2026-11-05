# vis-2026
Presentation initialized by Yixuan W.

Open [ivml-cost-benefit.html](ivml-cost-benefit.html) directly in a browser. The presentation is self-contained: no server, build step, or network is needed.

The revised talk responds to Ross's [round-one feedback](round1-feedback.txt) by following a skeptical stakeholder choosing between workflows for neuronal mitochondria analysis. Its central question is: **What additional value does a proposed visualization create over credible alternatives, and when is that value worth its additional cost?**

There are 14 main slides, 23 backups, and 1,334 words of main-talk speaker notes. The current draft targets 12:00 for a ten-minute slot; it includes expanded transition explanations and still needs trimming. At 120 words per minute, the notes take about 11:07, leaving roughly 53 seconds for pointing and pauses within the draft target. Rehearse against the per-slide targets, particularly the comparison and threshold slides. The opening overview allows 60 seconds; the returns allow 50 and 55 seconds to explain how the preceding section leads to the next.

- Left/Right or Space navigates the talk and stops at slide 14.
- **G** opens the overview: use the section links above the previews to jump to a backup topic. Section headers show the backup ranges, and each backup slide repeats its topic in the header.
- Choose backups for questions; **Return to the talk** restores the last main slide.
- **P** opens synchronized presenter notes with slide targets and cumulative finish times.
- **N** toggles notes, **F** toggles fullscreen, and the theme control switches light/dark mode.

| Slide | Message | Target | Finish by |
| --- | --- | --- | --- |
| 1 | Cost-Benefit Modeling of IVML Systems | 25s | 0:25 |
| 2 | Useful compared with what? | 35s | 1:00 |
| 3 | Overview - Compare workflows | 60s | 2:00 |
| 4 | Which workflow should the lab invest in? | 55s | 2:55 |
| 5 | We can reason with incomplete evidence. | 45s | 3:40 |
| 6 | Return to overview - Model value | 50s | 4:30 |
| 7 | Every workflow needs the same cost-benefit ledger. | 60s | 5:30 |
| 8 | Model updates also consume expert attention. | 45s | 6:15 |
| 9 | Covering its costs does not make it the best choice. | 70s | 7:25 |
| 10 | How much must the extra improvement be worth? | 85s | 8:50 |
| 11 | Repeated use can change the decision. | 50s | 9:40 |
| 12 | Return to overview - Test the contribution | 55s | 10:35 |
| 13 | What evidence would make the contribution convincing? | 50s | 11:25 |
| 14 | Make the value of a new workflow explicit. | 35s | 12:00 |

Slide 1 foregrounds the full paper title, with "Machine Learning" kept together and the stakeholder question visible immediately as a subtitle. Its title, question, and author block form a compact, vertically centered composition. The title-slide counter is omitted, and the ASU logo displays only the university mark from the embedded lockup. After the evaluation problem, slide 3 asks **"When is a new visualization worth using?"** It follows one lab's choice of tools through three questions: what the tool adds over alternatives, whether the improvement is worth the time and money, and what still needs measuring. The same questions return on slides 6 and 12, marking completed sections and highlighting the next one. The overview notes follow the visible questions in order and explain why each leads to the next. Slide 6 moves from comparing tools to weighing the improvement against its cost; slide 12 connects those two questions to the evidence still needed. Workflow details and numerical examples are discussed on the slides that display them. Where space allows, content-slide footers track these sections and underline the current one. Slide 4 omits the progress footer to give the example more room. The closing recap follows the same sequence.

Slide 4 introduces the lab director's decision and three workflows: manual work, a proposed image editor with a separate training script (A), and the MitoVis workflow (V). Slide 5 explains why a cost model helps when evidence is incomplete. A sparse upper row starts with available evidence and reveals explicit assumptions; the second reveal introduces the large question, "When would V be worth more than A?" The supporting line asks which assumptions change the choice. The notes ground this modular approach in paper Secs. 5-6 and retain its limits: answers are conditional, empirical comparison is needed to establish an advantage, and the paper does not claim end-to-end evaluation is prohibitive. Prioritizing measurements that could change the choice is the talk's inference from the framework. Slide 6 carries that uncertainty into the cost-benefit model. Slides 7-8 build the ledger from that decision, including expert reorientation after model updates. Slides 9-11 work through explicitly hypothetical costs and outcomes for A, a value threshold, and reuse. Slide 13 states the evidence needed to evaluate the contribution. The closing thank-you slide includes Rolando's faculty-job-market line. The title-slide definition is in the spoken introduction.

Citations and detailed qualifications are in reference-only speaker-note paragraphs, available through **N** or **P** and excluded from spoken-word counts and next-slide previews. Essential assumptions stay beside their values: slide 9 includes shared manual-work credit and assumed other costs as table rows, and slide 11 states the recurring gain, runtime cost, and adoption-cost assumptions before revealing reuse estimates. Figure captions retain figure numbers and axis details. The slides use a single progress footer without a second source footer.

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

A is a proposed workflow using a scientific image editor and a separate training script. A concrete implementation could use [napari, a viewer and editor for scientific images](https://napari.org/stable/howtos/layers/labels.html), with editable label layers over microscopy images for correcting boundaries and relabeling regions. One controlled study could start with the same predictions as V, inspect and edit masks and neurite labels in the editor, save corrected neurite labels, run a separate script to fine-tune the same classifier, then load its new predictions. The editor can also support manual annotation; A is ML-assisted because the model supplies initial annotations and learns from the corrections. The comparison asks whether MitoVis's [visual guides suggesting similar neurites to inspect and integrated correction/update loop](https://ieeevis.b-cdn.net/vis_2022/posters/v-vis-posters-1021-summary.pdf) justify their additional cost. Connecting the editor's corrected labels to the classifier requires integration work that must be measured. A's costs and outcomes remain invented teaching inputs. Supporting an empirical claim about A versus V would require implementing and testing A. A local decision can begin with available evidence, practical alternatives, and explicit uncertainty, then target the gaps that could change the choice. Paper Sec. 6 supports selecting relevant model terms, using measurements, literature baselines, logs, or sensitivity ranges under realistic project constraints. It complements empirical evaluation; it does not establish that a full comparison is prohibitive or validate the model's predictive accuracy. Matching the starting model and training recipe can help investigate the workflow's contribution; it is not a universal prerequisite for choosing a tool. Budget evidence gathering separately from the costs of adopting and using each workflow.

A is introduced for this talk; our cost-benefit paper does not evaluate it. The [2021 MitoVis preprint](https://arxiv.org/pdf/2109.01351), Secs. 3.2 and 5, describes a manual ImageJ-and-Excel reference. The [published journal abstract](https://pure.korea.ac.kr/en/publications/mitovis-a-unified-visual-analytics-system-for-end-to-end-neuronal/) reports up to 13.3 times faster analysis against a conventional manual workflow. The full journal text was inaccessible during this check, so additional algorithm comparisons or ablations remain unverified. The preprint and journal article are different versions; keep their reported results separate.

Slide 9 rounds dollars for readability and adds a V - A column so the extra cost and improvement are visible. Exact values remain in backup 01 and below. Both A and V receive the same $1,148.40 avoided-manual-work credit and use the same value U per percentage point of downstream classifier improvement. Count model utility beyond the corrected outputs so the same outcome is not credited twice. With all other incremental costs assumed zero:

- Net V = $1,148.40 + 10.1U - $10,123.08.
- Net A = $1,148.40 + 8.1U - $8,083.08.
- At U = $1,000/point, V returns $1,125.32 and A returns $1,165.32: V pays off against manual work but trails A by $40.
- V's additional net value is 2U - $2,040. The choice reverses at U = $1,020/point. At U = $1,500/point, V leads by $960.

Slide 10 uses an editable SVG with linear axes to show this crossing. It repeats V's extra $2,040 cost and 2-percentage-point classifier accuracy gain, defines one percentage point with an 80% -> 81% accuracy example, and spells out the unit in the axis and example labels. The speaker notes explain each calculation at its reveal step. Its "A ahead" and "V ahead" regions rank those two workflows; manual work remains another option, especially when both modeled net values are negative. It asks the stakeholder for a defensible range, rather than requiring an exact valuation. A range crossing the threshold leaves the choice unresolved. For insight without a defensible monetary value, connect knowledge to a decision or avoided loss, retain uncertainty, or compare effort to a defined knowledge outcome.

Slide 11 spreads the hypothetical additional $2,000 development cost across N independent workloads. Assuming the extra $40 runtime cost and 2-point gain recur on each workload, the threshold becomes ($2,000/N + $40) / 2: $1,020 at N=1, $120 at N=10, and $30 at N=100. The formula is retained in backup 01; the main slide emphasizes the thresholds and assumptions. These projections assume no additional learning or maintenance cost. Each workload must separately realize its benefit; repeatedly using one improved model does not automatically generate a new accuracy gain. Reuse projections do not establish lasting impact.

The 23 backups are grouped under six section headers in Grid. The section links stay above the scrolling previews so topics are easy to reach during questions. Slide numbers and arrow-navigation order are preserved.

| Backups | Section | Detail |
| --- | --- | --- |
| 01-02 | Comparison and valuation | Comparison assumptions, arithmetic, reuse, and the value of insight. |
| 03-05 | Worked examples and stopping | MitoVis break-even, fixed-model failure prevention, and stopping-time figures. |
| 06-11 | Workflow and interaction targets | Unified workflow, Van Wijk's foundation, and data, model, and understanding targets. |
| 12-15 | Cost-benefit equations | Total model, cost decomposition, training, re-alignment, and benefit pathways. |
| 16-20 | Applying the framework | Application by interaction target, variable mapping, and feedback-loop value. |
| 21-23 | Assumptions and calculations | Inputs and calculations behind the paper's thresholds and stopping times. |

Each backup's `data-backup-section` supplies its Grid grouping and presenter label; keep the matching slide header aligned when editing. No section-divider slides are added, so existing slide links and backup references keep their numbers.

The original MitoVis threshold of about $889 per point remains in backup 03 with its manual reference. It answers a different question from the main talk's $1,020 comparative threshold. The fixed-model audit's $10,038 threshold and the stopping-time curves also remain conditional worked examples. Neither ranks alternative solutions to the MitoVis task.

Supporting text uses near-black in light mode and near-white in dark mode across the main talk and backups, including captions, progress footers, table labels, and editable chart annotations. A shared slide text color keeps plain and tinted panels consistent. Preserve hierarchy through size and weight rather than low-contrast gray.

Embedded image assets and offline presentation behavior are preserved. Slide IDs are consecutive; main/backup counts and presenter timing derive from slide metadata. Keep visible content, source assumptions, and each slide's speaker-notes template together when editing. Use `notes-reference` paragraphs for citations and reference details; keep them separate from spoken notes and reveal cues.
