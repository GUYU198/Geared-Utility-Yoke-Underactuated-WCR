# First Weekly Report — Main Body

**Reporting period:** Week 1  
**Prepared by:** Ma Xiangzhuo (credited as the responsible author in the source slide deck)  
**Technical scope:** Part III — mechanical design of the magnetic table assembly, magnetic-circuit simulation, theoretical force analysis, and vehicle-body material selection  
**Companion material:** `Appendix - Illustrations/` (14 figures cropped from the Week-1 presentation)

> **Note on illustrations and language.** Every figure in this report is cropped directly from the Week-1 PowerPoint slides. The Chinese lettering that appears inside the images belongs to the original source material and is preserved without modification. Because the target repository uses English as its working language, a short English annotation is supplied immediately beneath each figure to render the source-slide content accessible to an English-speaking reader. Except for the unmodified screenshot content, all text in this document is written in English.

---

## 1. Executive Summary

The first week of the project was devoted to establishing the structural and magnetic design basis of the magnetic table assembly and to defining the preliminary vehicle-body material scheme. The principal outcomes are as follows.

1. The Week-1 technical presentation was prepared, and the Part III work programme was structured into six work packages: presentation preparation, innovative mechanical design of the magnetic table, two- and three-dimensional mechanical modelling, magnetic-array design, theoretical derivation of the air-gap–pull-off-force relation, and vehicle-body material analysis with preliminary scheme definition.
2. A dimensioned cross-section of the magnetic table was developed. The design uses a Q235 yoke beam, three N42 neodymium magnets in a 20 × 5 mm format, 6 mm inter-magnet spacing, Q235 spacers, and 3 mm copper fasteners, with a nominal overall width of 90 mm.
3. A two-dimensional finite-element magnetic-circuit workflow based on Finite Element Method Magnetics (FEMM) was established. Three variables were controlled: the yoke, the magnet-array arrangement, and the bolt material. Flux-line diagrams, flux-density maps, and equi-flux contours were generated for each configuration.
4. Simulation results consistently favour an alternating N–S–N array combined with a Q235 closed yoke and non-magnetic copper bolts. This arrangement concentrates the main flux on the working face and suppresses leakage towards the rear-side components.
5. The three-dimensional assembly was modelled in AutoCAD and SolidWorks. An exploded configuration identified the six-magnet array, the perforated Q235 yoke, and a plastic holder. The holder provides dual constraint: it prevents misalignment caused by strong mutual attraction during assembly and uses protruding stops to enforce the minimum air gap.
6. A theoretical air-gap–pull-off-force model was derived for yoke thicknesses of 0 mm, 1.5 mm, and 3 mm. A 3 mm yoke was selected as a compromise among magnetic strength, mechanical strength, and structural lightness. All force values obtained from this model are **theoretical estimates**, not measured data.
7. A strict safety rule was recorded: no steel-plate attraction test may be performed on the complete six-magnet assembly without protective measures and formal review. Experimental validation is scheduled for Week 3.
8. Material selection was narrowed, on a constant-mass basis, to a Q235 yoke, Q235 spacers, an acrylic (PMMA) base plate, and a PETG three-dimensionally printed housing.

---

## 2. Work Programme and Deliverables of Week 1

The Part III divider slide defined the scope of the week and associated each task with a specific engineering output.

![Figure 1. Overview of the Week-1 technical work packages and principal outputs.](<Appendix - Illustrations/Fig_01_Work_Overview.png>)

**Figure 1.** Overview of the Week-1 technical work packages and principal outputs. *(Source: Part III section divider of the Week-1 presentation; cropped.)*

> **English annotation of the source slide:** The divider identifies Part III as the most technically demanding section of the week. Its bullet list names six tasks: preparation of the weekly-report presentation; innovative mechanical design of the magnetic table; two- and three-dimensional mechanical modelling; magnetic-array design; theoretical derivation of the air-gap–pull-off-force curve; and vehicle-body material analysis with scheme definition. The four illustrations at the right-hand side show, from top to bottom, a FEMM flux-density contour map, an exploded view of the magnetic assembly, a family of theoretical pull-off-force curves, and the dimensioned cross-section of the magnet–yoke stack.

The deliverables associated with these tasks are: (i) the Week-1 presentation; (ii) a dimensioned two-dimensional section drawing; (iii) a three-dimensional assembly model and an exploded view; (iv) a set of FEMM comparison cases; (v) a theoretical force model with parametric curves; and (vi) a material-comparison table with a preliminary selection.

---

## 3. Mechanical Configuration of the Magnetic Table Assembly

### 3.1 Cross-section and dimensional definition

The mechanical section of the magnetic table was fixed before the magnetic analysis so that the electromagnetic model and the CAD model would share one geometry. The nominal overall width is 90 mm. A Q235 yoke beam of 78 × 3 mm carries three N42 permanent magnets, each 20 × 5 mm, with 6 mm gaps between adjacent magnets and 3 mm offsets at the two ends. Two Q235 spacers of 3 × 15 mm are placed at the ends, and the connection is made with 3 mm copper bolts. The coordinate convention uses the centre of the main beam as the origin of the x-axis and the lower surface of the main beam as y = 0; all dimensions are in millimetres. The specified assembly direction places the magnets above the beam and the screws below it, with a 1.5 mm head projection relative to the yoke reference surface.

![Figure 2. Dimensioned cross-section of the magnetic table assembly.](<Appendix - Illustrations/Fig_02_Magnetic_Assembly_Cross_Section.png>)

**Figure 2.** Dimensioned cross-section of the magnetic table assembly. *(Source: section 3.1, mechanical design of the magnetic-table assembly; cropped.)*

> **English annotation of the source slide:** The red blocks on the upper side of the beam are the N42 neodymium magnets, three in total, each labelled with its material grade. The blue horizontal member is the Q235 yoke beam; the brown vertical elements at the two ends are Q235 spacers, and the small domed heads at the ends are the fasteners. The dimensional chain at the top gives 3 mm end offsets, three 20 mm magnet lengths, and two 6 mm gaps. The legend at the lower left lists the four part categories and their quantities; the note at the lower right defines the coordinate system, the unit, and the assembly direction.

### 3.2 Design intent of the section

Three consequences follow directly from the section geometry. First, the 6 mm spacing separates the magnets sufficiently to make the array arrangement an independent design variable rather than a manufacturing accident. Second, the 3 mm yoke thickness is thin enough to keep the assembly light while remaining a practical machined plate. Third, the end spacers and the holder (Section 5.2) translate the nominal geometry into a repeatable physical gap, which is essential because the theoretical model shows an extremely steep force decay with increasing air gap (Section 7).

---

## 4. Magnetic-Circuit Design and FEMM Simulation

### 4.1 Simulation workflow and controlled variables

A two-dimensional finite-element magnetic analysis was performed with Finite Element Method Magnetics (FEMM). The study intentionally limited itself to three controlled variables so that each simulation could be attributed to a single cause:

1. **Yoke condition** — plastic support versus a low-carbon Q235 steel yoke;
2. **Magnet-array arrangement** — alternating polarity versus identical polarity facing the working face;
3. **Fastener material** — magnetically conductive steel versus non-magnetic copper.

For every case, the software produced flux-line diagrams, flux-density contour maps, and equi-flux plots. These three representations are complementary: flux lines show the topological path of the field, the contour map quantifies local flux density, and the equi-flux plot reveals leakage towards non-working surfaces.

![Figure 3. FEMM workflow and representative output sets for the four principal cases.](<Appendix - Illustrations/Fig_03_FEMM_Magnetic_Circuit_Workflow.png>)

**Figure 3.** FEMM workflow and representative output sets for the four principal cases. *(Source: section 3.2, magnetic-circuit design; cropped.)*

> **English annotation of the source slide:** The left-hand bullet list states that three variables are controlled — the yoke, the magnet-array arrangement, and the bolt material — and that the professional finite-element software FEMM was used to draw flux-line diagrams, flux-density maps, and equi-flux lines. The right-hand side contains four pairs of results. Each pair places a flux-line diagram on the left and a colour-coded flux-density contour map on the right, allowing the effect of each variable to be compared case by case.

### 4.2 Array arrangement without a yoke

With a plastic support and no yoke, two arrangements were compared. In the alternating N–S–N configuration, adjacent opposite poles form arch-shaped closed loops; the flux path is continuous and smooth, and the main flux is delivered to the working face, giving high circuit utilisation. In the all-N configuration, like poles face one another, the flux lines are compressed against each other, the local flux density rises, and a large part of the main flux escapes towards the back of the assembly, giving low circuit efficiency. The flux-density maps for both no-yoke cases nevertheless show pronounced rear leakage and edge flux.

![Figure 4. Array comparison without a yoke: alternating polarity versus identical polarity.](<Appendix - Illustrations/Fig_04_No_Yoke_Array_Comparison.png>)

**Figure 4.** Array comparison without a yoke: alternating polarity versus identical polarity. *(Source: section 3.2.1, two array forms without a yoke, plastic support; cropped.)*

> **English annotation of the source slide:** The upper-left diagram and its text describe the alternating N–S–N arrangement, noting that adjacent opposite poles form arch-shaped closed loops, that the flux path is continuous and smooth, and that the main flux acts on the working face with high magnetic-circuit utilisation. The upper-right diagram describes the all-N arrangement, noting like-pole repulsion, compressed flux lines, increased local density, severe main-flux escape, and low efficiency. The two lower colour plots are flux-density maps; the caption under each states that rear leakage and edge flux are severe.

### 4.3 Effect of the yoke

Introducing the Q235 yoke changes the circuit topology decisively. With the plastic support, the circuit is semi-open: flux lines diverge along the non-working surfaces, edge flux is prominent, and the rear-side components are exposed to interference. With the Q235 yoke, the high-permeability steel forms a closed circuit that constrains flux within the intended path. Flux density in the working region rises markedly, while interference at the rear is strongly reduced.

![Figure 5. Influence of the yoke on the magnetic circuit: plastic support versus Q235 steel.](<Appendix - Illustrations/Fig_05_Yoke_Effect_Comparison.png>)

**Figure 5.** Influence of the yoke on the magnetic circuit: plastic support versus Q235 steel. *(Source: section 3.2.2, effect of the yoke; cropped.)*

> **English annotation of the source slide:** The left-hand case is the plastic-support configuration. Its text describes a semi-open circuit, strong divergence of flux along non-working surfaces, prominent edge flux, low circuit efficiency, and a strong influence on rear-side components. The right-hand case uses ordinary Q235 carbon structural steel. Its text describes a closed, high-permeability circuit, effective constraint of non-working flux, a marked rise of working-area flux density, improved efficiency, and minimal influence on rear components. The lower row gives the corresponding flux-density contour maps.

### 4.4 Array arrangement with a yoke

With the yoke installed, the two array arrangements were compared again. The alternating arrangement remains clearly superior to the identical-polarity arrangement, confirming that the benefit of the alternating pattern is independent of the yoke. The final configuration therefore combines an alternating N–S–N array with a Q235 closed yoke.

![Figure 6. Array comparison with a Q235 yoke installed.](<Appendix - Illustrations/Fig_06_With_Yoke_Array_Comparison.png>)

**Figure 6.** Array comparison with a Q235 yoke installed. *(Source: section 3.2.3, two array forms with a low-carbon Q235 yoke; cropped.)*

> **English annotation of the source slide:** The left pair of diagrams shows the alternating N–S–N arrangement and repeats the conclusion that adjacent opposite poles form arch-shaped closed loops with a continuous, smooth path and high utilisation of the main flux at the working face. The right pair shows the all-N arrangement and repeats the conclusion that like-pole repulsion compresses the flux lines, increases local density, and causes severe main-flux escape. The flux-density maps beneath confirm that the alternating case delivers a stronger, better-confined working field than the identical-polarity case.

### 4.5 Influence of fastener material

The third variable was the bolt material. Steel bolts are magnetically conductive and therefore create a low-reluctance bypass across the yoke. Flux is shunted through this bypass, local saturation occurs, rear-side interference increases, and the efficiency of the working circuit falls. Copper bolts are non-magnetic; they block the bypass path, direct the main flux into the working region, and produce minimal rear-side interference. Copper was therefore adopted for the connection bolts.

![Figure 7. Effect of bolt material on the magnetic circuit: steel versus copper.](<Appendix - Illustrations/Fig_07_Bolt_Material_Effect.png>)

**Figure 7.** Effect of bolt material on the magnetic circuit: steel versus copper. *(Source: section 3.2.4, effect of bolt material; cropped.)*

> **English annotation of the source slide:** The upper case is labelled as steel bolts and identified as magnetically conductive. Its note explains that a low-reluctance bypass forms, flux is shunted, local saturation is triggered, rear-side interference is aggravated, and field efficiency is reduced. The lower case is labelled as copper bolts and identified as non-magnetic; its note explains that the bypass is effectively blocked, the main circuit acts fully in the working region, and rear-side interference is low. The two colour plots show the corresponding flux-density distributions.

### 4.6 Summary of the magnetic design decision

The three simulated variables lead to one consistent design rule: **alternating N–S–N array + Q235 closed yoke + copper fasteners**. This combination maximises the flux density available at the working face while minimising flux that is wasted at the rear or diverted through structural hardware.

---

## 5. Three-Dimensional Mechanical Assembly

### 5.1 Assembly structure

The mechanical structure of the magnetic table was modelled in AutoCAD and SolidWorks. The model resolves the relative positions of magnets, yoke, holder, spacers, and fastening points, and provides the geometric basis for both the engineering drawing and the subsequent prototype.

![Figure 8. Three-dimensional structure of the magnetic-table assembly.](<Appendix - Illustrations/Fig_08_Magnetic_Assembly_3D.png>)

**Figure 8.** Three-dimensional structure of the magnetic-table assembly. *(Source: section 3.3, mechanical design structure; cropped.)*

> **English annotation of the source slide:** The slide states that the magnetic-table assembly structure was drawn with AutoCAD and SolidWorks. The rendering shows the assembled frame, the rectangular recesses that receive the magnets, the transverse yoke, and the fastening points at the outer frame. The small axis markers in the image indicate the modelling coordinate directions.

### 5.2 Exploded view and functional integration

The exploded view separates the assembly into three essential groups: six N42 NdFeB magnets, the Q235 yoke with pre-drilled assembly holes, and the plastic holder. The holder addresses two practical problems at once. First, the strong mutual attraction between neighbouring magnets makes manual placement prone to misalignment; the holder locates each magnet before the magnetic forces can pull it out of position. Second, protruding stops on the holder define the minimum air gap, so that the nominal gap assumed in the theoretical model can be reproduced physically.

![Figure 9. Exploded view of the magnetic-table assembly.](<Appendix - Illustrations/Fig_09_Assembly_Exploded_View.png>)

**Figure 9.** Exploded view of the magnetic-table assembly. *(Source: section 3.3.1, exploded view; cropped.)*

> **English annotation of the source slide:** The left-hand bullet list names the three separated elements: the plastic holder, which simultaneously constrains the magnets and the air gap; the array of six N42 NdFeB strong magnets; and the Q235 yoke with reserved assembly holes. The notes at the right-hand side give three engineering reasons for the scheme. First, magnetic efficiency is improved by the alternating array and Q235 closed yoke, which increase working-face flux and reduce rear leakage. Second, mechanical reliability is improved because the plastic holder solves assembly difficulty and misalignment caused by strong attraction, while protruding stops control the minimum air gap and ensure structural safety. Third, manufacturing is feasible because the modular design is easy to fabricate and the reserved holes allow integral assembly.

The assembly strategy can therefore be summarised in three clauses: the magnetic circuit is secured by the alternating array and the yoke, the mechanical stability is secured by the holder, and manufacturability is secured by modularisation.

---

## 6. Theoretical Derivation of the Air-Gap–Pull-Off Relation

### 6.1 Rationale for the 3 mm yoke

The yoke thickness was not chosen arbitrarily. A thicker yoke improves the magnetic circuit and the pull-off force, but it also increases mass and manufacturing cost. A thinner yoke saves weight but is harder to machine reliably and may saturate. The adopted 3 mm value is the result of a three-way trade-off among magnetic strength, mechanical strength, and structural lightness. The derivation was carried out with an explicit physical model; the complete set of formulae and the step-by-step derivation are retained in the appendix of the original presentation and are therefore not reproduced here.

### 6.2 Parametric theoretical curves

Three families of theoretical curves were computed: no yoke, a 1.5 mm yoke, and a 3 mm yoke. Each family plots the vertical pull-off force *F* in newtons against the air gap *g* in millimetres. Within each family, four steel-plate thicknesses (0.5, 1, 2, and 3 mm) and two array arrangements are superposed: solid lines denote the alternating arrangement and dashed lines the identical-polarity arrangement, while colour identifies the plate thickness.

![Figure 10. Theoretical pull-off-force curve for the configuration without a yoke.](<Appendix - Illustrations/Fig_10_AirGap_PullOff_NoYoke.png>)

**Figure 10.** Theoretical pull-off-force curve for the configuration without a yoke. *(Source: section 3.4, theoretical derivation, no-yoke curves; cropped.)*

> **English annotation of the source slide:** The chart title identifies the no-yoke case and the four plate thicknesses crossed with two array arrangements. Its subtitle states that solid lines correspond to the alternating arrangement, dashed lines to the identical-polarity arrangement, and colour to plate thickness. The horizontal axis is the vertical pull-off force in newtons and the vertical axis is the air gap in millimetres.

![Figure 11. Theoretical pull-off-force curve for a 1.5 mm yoke.](<Appendix - Illustrations/Fig_11_AirGap_PullOff_Yoke_1p5mm.png>)

**Figure 11.** Theoretical pull-off-force curve for a 1.5 mm yoke. *(Source: section 3.4, theoretical derivation, 1.5 mm yoke curves; cropped.)*

> **English annotation of the source slide:** The title identifies the configuration as a 1.5 mm yoke with four plate thicknesses and two array arrangements. The subtitle gives the same line-style convention as Figure 10: solid for alternating, dashed for identical polarity, and colour for plate thickness. The axes give pull-off force in newtons and air gap in millimetres.

![Figure 12. Theoretical pull-off-force curve for a 3 mm yoke.](<Appendix - Illustrations/Fig_12_AirGap_PullOff_Yoke_3mm.png>)

**Figure 12.** Theoretical pull-off-force curve for a 3 mm yoke. *(Source: section 3.4, theoretical derivation, 3 mm yoke curves; cropped.)*

> **English annotation of the source slide:** The title identifies the 3 mm yoke case, again with four plate thicknesses and two array arrangements. The subtitle states that solid curves denote the alternating arrangement, dashed curves the identical-polarity arrangement, and colours the plate thickness. The horizontal axis is pull-off force in newtons and the vertical axis is the air gap in millimetres.

Reading the three families together shows the same trend as the FEMM study: alternating arrays give substantially larger pull-off forces than identical-polarity arrays, and increasing the yoke thickness raises the achievable force. It also shows that every curve decays steeply as the air gap increases.

---

## 7. Influencing Factors, Conclusions, and Safety Boundary

### 7.1 Factors considered

Four factors were identified as dominant in the theoretical model: yoke thickness, steel-plate thickness, air-gap size, and array arrangement. The model attempts to include the majority of relevant influences, but it is still a simplification of the physical system; the source slide explicitly states that theoretical estimates differ from real-world behaviour and that actual measurements are required.

![Figure 13. Dominant influencing factors and the conclusions drawn from the 3 mm yoke curves.](<Appendix - Illustrations/Fig_13_Influence_Factors_And_Conclusions.png>)

**Figure 13.** Dominant influencing factors and the conclusions drawn from the 3 mm yoke curves. *(Source: section 3.4.1, principal factors influencing magnetic force; cropped.)*

> **English annotation of the source slide:** The left-hand list names four factors: yoke thickness, steel-plate thickness, air-gap size, and array arrangement. The small footnote states that, although most influencing factors were considered, theoretical estimates cannot fully reproduce real conditions and therefore serve only as a reference for the scheme; the team plans real experiments based on actual hardware to obtain objective values. The chart uses the same conventions as Figure 12. The three notes on the right state that the calculations confirm the FEMM conclusion that the alternating array gives a much larger pull-off force; that local magnetic saturation causes the force to increase markedly with plate thickness, reaching a theoretical zero-gap value of about 150 jin, accompanied by a strict prohibition on unprotected and unreviewed steel-plate attraction tests on the complete six-magnet assembly; and that the pronounced nonlinear decay with air gap demonstrates the importance of the holder limit and gap control.

### 7.2 Conclusions

1. **Array arrangement.** The alternating arrangement gives a much larger pull-off force than the identical-polarity arrangement. This agrees with the FEMM simulations and removes the need to consider the same-polarity layout further.
2. **Plate and yoke thickness.** Increasing the steel-plate thickness raises the pull-off force because of the changing saturation state. At the theoretical zero-air-gap limit the model reaches approximately **150 jin** (about 75 kgf, or roughly 735 N). This number is a **theoretical estimate only** and must never be reported as a measured result.
3. **Air gap.** All curves show a steep, nonlinear decay with increasing air gap. This is the direct reason why the holder must control the minimum gap with mechanical stops.
4. **Validation status.** No experimental measurement has yet been made. Week 3 is reserved for physical tests that will compare measured pull-off forces with the theoretical curves.

### 7.3 Safety boundary

The source slide defines a hard safety red line: under no circumstances may a steel-plate attraction test be carried out on the complete six-magnet assembly without protective measures and without formal review. The estimated zero-gap force is large enough that an uncontrolled attraction event could injure personnel or damage the assembly. All future tests must be planned around a controlled gap, guarded handling, and an approved procedure.

---

## 8. Material Strength Analysis and Preliminary Selection

### 8.1 Evaluation method

Two questions governed the material study: whether the final product can work under the actual service conditions, and whether the vehicle mass remains acceptable. The decisive failure modes for load-bearing parts are fracture, interlaminar cracking, and creep. Following the principle of controlling weight while preserving strength, the mass was held constant and only the material and the equal-mass thickness were changed. Yield strength and elastic modulus were then calculated, and price, machining difficulty, and cracking risk were added to the comparison.

### 8.2 Preliminary material scheme

The preliminary scheme selects Q235 for the yoke and the spacers, acrylic (PMMA) for the base plate, and PETG for the three-dimensionally printed housing. The relevant source data are summarised below.

| Component | Preliminary material | Density (g/cm³) | Equal-mass thickness (approx., mm) | Strength indicator | Elastic modulus (GPa) | Main risk noted in the source |
|---|---|---:|---:|---|---:|---|
| Yoke | Q235 low-carbon steel | 7.85 | 1.6 | Yield 235 MPa (plate ≤ 16 mm) | 200–210 | Good ductility and low cracking risk; fatigue must be checked under long-term cyclic load |
| Spacer | Q235 low-carbon steel | 7.85 | 1.6 | Yield 235 MPa (plate ≤ 16 mm) | 200–210 | Same as the yoke |
| Base plate | Acrylic (PMMA) | 1.19 | 10.5 | Flexural strength about 124 MPa; tensile fracture about 76 MPa | 2.76 | Solvent- or internal-stress cracking; notch sensitivity |
| Housing | PETG (printed) | 1.23–1.27 | 10.2 | Tensile strength 40–55 MPa | 2.0–2.4 | Layer adhesion and notch effects; creep deformation at elevated temperature |

**Table 1.** Preliminary material selection derived from the Week-1 material comparison.

![Figure 14. Material comparison table used for the strength and mass study.](<Appendix - Illustrations/Fig_14_Material_Strength_Comparison.png>)

**Figure 14.** Material comparison table used for the strength and mass study. *(Source: section 3.5, material strength analysis; cropped.)*

> **English annotation of the source slide:** The introductory text explains that the decision is governed by vehicle mass and by the strength of load-bearing parts, specifically fracture, interlaminar cracking, and creep; the method is to keep mass constant, change only the material and equal-mass thickness, calculate yield strength and elastic modulus, and then add price and cracking risk. The table lists candidate materials with columns for density, equal-mass thickness, strength, elastic modulus, processing difficulty, and principal cracking risk. Its rows include carbon-fibre sheet, TC4 titanium alloy, 7075-T6 aluminium, high-carbon T10 steel, GFRP, 6061-T6 aluminium, Q235 low-carbon steel, PMMA, and several three-dimensionally printed polymers. The concluding sentence states the preliminary choices: Q235 yoke, Q235 spacer, acrylic base plate, and PETG printed housing.

### 8.3 Interpretation

Q235 offers a high modulus and a clearly defined yield point at low cost, which suits the yoke and the spacers where dimensional stability matters more than mass. PMMA and PETG have much lower densities, so their equal-mass thicknesses are roughly an order of magnitude larger; this is acceptable for the base plate and housing, where stiffness requirements are modest, but it introduces solvent cracking and creep risks that must be addressed in the detailed design. The selection remains preliminary and will be revisited after prototype testing.

---

## 9. Risk Register and Planned Follow-up

| Item | Current status | Planned action |
|---|---|---|
| Magnetic-array performance | Established by FEMM and theoretical curves; not measured | Fabricate the alternating array and confirm the working-face field in Week 3 |
| Air-gap repeatability | Defined by holder stops in CAD | Verify manufactured stop height and measure the assembled gap |
| Pull-off force | Theoretical estimate only, including the zero-gap value | Conduct guarded, reviewed measurements in Week 3 and compare with Figures 10–13 |
| Fastener bypass | Copper selected to suppress the magnetic shunt | Confirm the installed fastener material on the prototype |
| Material cracking and creep | Identified as risks in the comparison table | Review processing conditions and joint details before final manufacture |
| Safety | Red line documented | Enforce protective measures and formal approval before any attraction test |

---

## 10. Appendix A — Illustration Manifest

All illustration files are stored in `Appendix - Illustrations/` and are referenced in this document with forward-slash relative paths.

| Figure | File name | Source section | English annotation summary |
|---|---|---|---|
| 1 | `Fig_01_Work_Overview.png` | Part III divider | Work-package list plus overview of FEMM map, exploded view, force curves, and section |
| 2 | `Fig_02_Magnetic_Assembly_Cross_Section.png` | 3.1 | Magnets, yoke, spacers, fasteners, dimensions, and coordinate convention |
| 3 | `Fig_03_FEMM_Magnetic_Circuit_Workflow.png` | 3.2 | Three controlled variables and four pairs of flux-line and flux-density results |
| 4 | `Fig_04_No_Yoke_Array_Comparison.png` | 3.2.1 | Alternating versus identical polarity without a yoke; rear leakage noted |
| 5 | `Fig_05_Yoke_Effect_Comparison.png` | 3.2.2 | Plastic semi-open circuit versus Q235 closed circuit |
| 6 | `Fig_06_With_Yoke_Array_Comparison.png` | 3.2.3 | Array comparison repeated with the Q235 yoke installed |
| 7 | `Fig_07_Bolt_Material_Effect.png` | 3.2.4 | Conductive steel bypass versus non-magnetic copper bolt |
| 8 | `Fig_08_Magnetic_Assembly_3D.png` | 3.3 | AutoCAD and SolidWorks assembly rendering |
| 9 | `Fig_09_Assembly_Exploded_View.png` | 3.3.1 | Six magnets, Q235 yoke, plastic holder, and engineering rationale |
| 10 | `Fig_10_AirGap_PullOff_NoYoke.png` | 3.4 | Theoretical curves without a yoke |
| 11 | `Fig_11_AirGap_PullOff_Yoke_1p5mm.png` | 3.4 | Theoretical curves with a 1.5 mm yoke |
| 12 | `Fig_12_AirGap_PullOff_Yoke_3mm.png` | 3.4 | Theoretical curves with a 3 mm yoke |
| 13 | `Fig_13_Influence_Factors_And_Conclusions.png` | 3.4.1 | Four influencing factors, curve conclusions, and safety note |
| 14 | `Fig_14_Material_Strength_Comparison.png` | 3.5 | Material-property comparison and preliminary selection |

---

## 11. Appendix B — Note on Quantitative Claims

The figure of approximately 150 jin at zero air gap is a result of the theoretical derivation presented in Section 3.4 of the source slides. It is an estimate obtained from an analytical model under idealised assumptions and has not been verified experimentally. It is recorded here only as a design reference and as the motivation for the safety boundary in Section 7.3. All experimental values will be reported separately after the Week-3 tests.
