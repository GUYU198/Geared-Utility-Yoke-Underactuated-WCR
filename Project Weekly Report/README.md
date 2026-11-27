# Project Weekly Report

## 1. Purpose and Scope

This directory contains the chronological weekly technical record of the **Geared-Utility-Yoke-Underactuated-WCR** project. It is maintained as a version-controlled archive of interim results, design decisions, theoretical work, simulation outputs, and material studies produced during the project cycle. Each weekly report is intended to be a self-contained academic document that records what was investigated, what was established, what remains uncertain, and how the work connects to the following week.

The reports in this directory are working records of the author. They are not, by themselves, the final deliverables of the project. In accordance with the statement in the repository root, only material that has been sufficiently reviewed and validated will be transferred to the project team's master repository as formal deliverables.

## 2. Project Context

The project concerns a dual-motor magnetic wall-climbing robotic vehicle that combines magnetic adhesion with an underactuated mechanism design. The adhesion module uses an array of N42-grade NdFeB permanent magnets mounted on a Q235 carbon structural steel yoke, with controlled adjustment of the magnetic-circuit air gap to balance adhesive force against motion resistance. The drive and control layer adopts an encoder-based differential drive implemented on an ESP32 microcontroller. Gear transmission and underactuated manipulation are combined to obtain a compact, lightweight platform capable of operating on ferromagnetic surfaces.

- **Institution:** Shenzhen Polytechnic University (SZPU)
- **Individual workspace:** [Geared-Utility-Yoke-Underactuated-WCR](https://github.com/GUYU198/Geared-Utility-Yoke-Underactuated-WCR)
- **Project team master repository:** [Track-B-Magnetic-wall-Climber](https://github.com/wanlin050/Track-B-Magnetic-wall-Climber)

Related technical material in this repository includes the mechanical structure models under [`../Mechanial-Structure/`](<../Mechanial-Structure/>) and the theoretical calculations and reports under [`../Air Gap - Pull-off Force Curve/Theoretical Calculations and Reports/`](<../Air Gap - Pull-off Force Curve/Theoretical Calculations and Reports/>). The weekly reports synthesize progress across these and other work packages.

## 3. Reporting Period and Update Cadence

The reporting sequence covers approximately **one and a half months**, organised as six weekly cycles. A new report is added at the end of each week under a directory named `Week N`. The Week 1 record establishes the design basis; subsequent reports are expected to document prototype development, experimental validation, integration, and final consolidation.

As of the current version of this index, **Week 1 is available** and Weeks 2–6 are planned. The status column in Section 5 is updated whenever a new report is committed.

## 4. Directory Structure

```text
Project Weekly Report/
├── README.md
└── Week 1/
    ├── First Weekly Report - Main Body.md
    └── Appendix - Illustrations/
        ├── Fig_01_Work_Overview.png
        ├── Fig_02_Magnetic_Assembly_Cross_Section.png
        ├── Fig_03_FEMM_Magnetic_Circuit_Workflow.png
        ├── Fig_04_No_Yoke_Array_Comparison.png
        ├── Fig_05_Yoke_Effect_Comparison.png
        ├── Fig_06_With_Yoke_Array_Comparison.png
        ├── Fig_07_Bolt_Material_Effect.png
        ├── Fig_08_Magnetic_Assembly_3D.png
        ├── Fig_09_Assembly_Exploded_View.png
        ├── Fig_10_AirGap_PullOff_NoYoke.png
        ├── Fig_11_AirGap_PullOff_Yoke_1p5mm.png
        ├── Fig_12_AirGap_PullOff_Yoke_3mm.png
        ├── Fig_13_Influence_Factors_And_Conclusions.png
        └── Fig_14_Material_Strength_Comparison.png
```

A future weekly directory should follow the same pattern: one main Markdown document accompanied by a dedicated `Appendix - Illustrations/` folder. Binary assets are kept beside the document they support so that every report remains portable and independently readable.

## 5. Weekly Report Index

| Week | Principal focus | Main report | Status |
|---|---|---|---|
| 1 | Work-programme definition; magnetic-table cross-section; FEMM magnetic-circuit comparison; theoretical air-gap–pull-off derivation; preliminary material selection | [Week 1 main body](<Week 1/First Weekly Report - Main Body.md>) · [Illustrations](<Week 1/Appendix - Illustrations/>) | Available |
| 2 | To be added in the second weekly cycle | — | Planned |
| 3 | To be added in the third weekly cycle | — | Planned |
| 4 | To be added in the fourth weekly cycle | — | Planned |
| 5 | To be added in the fifth weekly cycle | — | Planned |
| 6 | To be added in the sixth weekly cycle | — | Planned |

The focus descriptions for Weeks 2–6 are placeholders and will be replaced with the actual technical scope when those reports are written.

## 6. Documentation Conventions

### 6.1 Report structure

Each weekly report is written as a structured Markdown document. A report normally contains an executive summary, a statement of the work package, the methods and models used, the results obtained, an explicit distinction between estimation and measurement, and a closing section on risks and follow-up work. Figures and tables are numbered consecutively and are referenced from the main text.

### 6.2 Language and figure annotation

The narrative text of the reports is written in academic English so that the documents remain readable in an international repository. Chinese lettering may remain where it is part of an unmodified source screenshot, such as a cropped presentation slide. In such cases, a concise English annotation is placed immediately below the figure to explain the source-slide content to an English-speaking reader.

### 6.3 Image naming and relative paths

Illustration files follow the pattern `Fig_NN_Descriptive_Name.png`, with `NN` as a two-digit sequential number and a short English description of the figure content. All image references in Markdown use relative paths with forward slashes. Because the directory names contain spaces, destinations are enclosed in angle brackets; for example:

```markdown
![Figure 1. Work-package overview](<Appendix - Illustrations/Fig_01_Work_Overview.png>)
```

This convention keeps links valid on Windows, macOS, Linux, and GitHub's web renderer.

### 6.4 Quantitative claims and provenance

Theoretical calculations, simulation outputs, and experimental measurements are reported as separate categories. Values derived from analytical models are explicitly labelled as theoretical estimates and must not be presented as measured results. The safety qualification attached to the Week 1 force estimate is retained wherever that estimate is discussed. Assumptions, controlled variables, and data sources are stated so that later weeks can reproduce or challenge the result.

## 7. Maintenance Workflow

1. Create a new directory named `Week N` for the corresponding week.
2. Place the main-body Markdown file and its `Appendix - Illustrations/` folder inside that directory.
3. Check that every figure reference resolves to an existing file using a forward-slash relative path.
4. Add or update the corresponding row in the index in Section 5, including the report status.
5. Commit the changes to the `main` branch with a message of the form `docs(weekly-report): add Week N report`.
6. When a result has been reviewed and validated, transfer the relevant material to the project team's master repository according to the project's formal procedure.

Before each commit, the report should be checked for figure-number continuity, consistent terminology, clear separation of estimated and measured values, and the presence of an English annotation for any figure that contains Chinese source text.

## 8. Status Statement

This README is an index and maintenance guide for the weekly-report archive. It records the reporting plan and the current state of the archive. Technical findings belong in the individual weekly reports and in the validated materials of the project team's master repository; they are not duplicated here.

*Initial version prepared for the six-week reporting cycle.*
