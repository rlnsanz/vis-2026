# vis-2026
Presentation initialized by Yixuan W

The self-contained presentation is `ivml-cost-benefit.html`. Open it directly in a browser; no server, build step, or network is needed.

The main talk has 15 slides and 945 words of speaker notes, with a 9:30 pacing target inside a 10-minute slot. At 120 words per minute, the notes take about 7.9 minutes to speak, leaving about 1.6 minutes within the target for pointing to figures, transitions, and pauses. Rehearse against the targets below to adjust to your delivery.

- Left/Right or Space navigates the main talk and stops at slide 15.
- **G** opens the overview, with the main talk first and 17 backup slides below it.
- Choose a backup slide for questions; **Return to the talk** in Grid restores your last main slide.
- **P** opens synchronized presenter notes, with each slide’s target duration and cumulative finish time.
- **N** toggles notes in the presentation window. **F** toggles fullscreen.

| Slide | Message | Target duration | Finish by |
| --- | --- | --- | --- |
| 1 | Cost-Benefit Modeling of IVML Systems | 20s | 0:20 |
| 2 | Better outcomes still have a cost. | 30s | 0:50 |
| 3 | Overview: From interaction to a design decision | 20s | 1:10 |
| 4 | A quality gain needs a task-specific value | 35s | 1:45 |
| 5 | Count the session and every update | 30s | 2:15 |
| 6 | What interaction changes determines the trade-off | 65s | 3:20 |
| 7 | Expected benefits must cover expected costs | 45s | 4:05 |
| 8 | Model updates also require people to reorient | 35s | 4:40 |
| 9 | Overview · Two cases | 10s | 4:50 |
| 10 | MitoVis: When do data and model improvements pay off? | 75s | 6:05 |
| 11 | A fixed model can create value through failure prevention | 60s | 7:05 |
| 12 | Overview · Design implications | 10s | 7:15 |
| 13 | Stop when the next interaction costs more than it adds | 75s | 8:30 |
| 14 | Design the workflow around the value you need | 35s | 9:05 |
| 15 | Better visual design earns more value with less interaction. | 25s | 9:30 |

The title slide focuses on the title, research question, and authors. Slide 2 follows one label correction in an illustrative defect classifier that sorts photos of machined parts into pass or defect. Slides 4–5 carry that scenario into a worked example: a 10-percentage-point accuracy gain on a 500-part batch, at about $4 per wrong call, is 50 fewer wrong calls and $200 in model benefit; relabeling, three retraining runs, and separate re-checking cost $55, leaving $145 to cover development. These are teaching inputs, not study results. Initial training is outside the example’s accounting boundary, view compute is assumed negligible, and only model-performance benefit is valued. Slide 6 then generalizes the example to the paper’s three interaction targets. Slide 8 grounds re-alignment cost in MitoVis: each update used about $0.02 of GPU time but about $3 of assumed expert re-orientation time.

Slide 3 provides a visual roadmap from the framework through the two case studies to design decisions, with Framework highlighted as the starting point. The full roadmap returns at slide 9 with Two cases highlighted and at slide 12 with Design implications highlighted. Each repeat has a 10-second target and its own transition notes. A section roadmap stays visible on the content slides: Framework on 4–8, Two cases on 10–11, and Design implications on 13–14. Slides 8 and 11 preview the next section. Main-talk section labels use 32px type; diagram labels and supporting content use at least 28px, while source footers and slide counters use 24px on the 1600 × 900 canvas. The opening diagrams and worked example use editable SVG and HTML. Original paper figures appear on slides 6, 10, 11, and 13. They retain their own typography, with larger slide text explaining the relevant paths, colors, and thresholds.

The paper figures are embedded directly from the PDF, so the deck remains self-contained:

- Slide 6: Figure 1 (p. 3), explained through the three return paths to data, model, and view.
- Slide 10: Figure 2, left panel (p. 7), explained through the axes, benefit/cost lines, and $889 crossing.
- Slide 11: Figure 3, left panel (p. 8), reuses that reading pattern for the $10,038 failure-value threshold.
- Slide 13: Figure 3, right panel (p. 8), follows the middle blue curve and explains the other two as discovery-rate sensitivity. The plotted times are not recommended audit durations.

The panels retain the original axes, ticks, and curves. Repeated panel headings and compact legends are cropped out; larger legends sit beside the plots. The original system screenshots are retained in backups 15 and 16. The notes include a short walkthrough for every figure, with 65, 75, 60, and 75 seconds allocated to these slides.

The main talk groups costs into development, human effort, and computation. It preserves the three interaction targets, four benefit pathways, model-update overhead, two case-study thresholds, and the distinction between break-even and stopping decisions. Backup slides retain the full workflows, notation, equations, configuration tables, original reference figures, and explicit assumptions behind the numerical results.

Ground truth: `IVML_Cost_Benefit_2026_VIS.pdf`, especially Sections 4 and 5. The case-study values are illustrative calculations based on published measurements and proxy assumptions. They are not measured financial returns.
