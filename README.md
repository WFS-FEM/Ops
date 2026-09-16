# WFS-FEM Ops

Planning and project-management home for operationalizing the **West Florida Shelf Fisheries Ecosystem Model (WFS-FEM)**, an Ecopath with Ecosim/Ecospace model used to estimate red tide mortality (M<sub>rt</sub>) for Gulf of America grouper stock assessments.

> **Operational = Automated + Integrated + Communicated**

## What this repository is for

This repository holds the plan, the cross-cutting issues, meeting records, decisions and the risk register. Model code lives in the other WFS-FEM repositories (below). The work itself is tracked in the organization project **[WFS-FEM Operationalization](https://github.com/orgs/WFS-FEM/projects/4)**, which pulls in issues from every repository.

## Objectives

| | Objective | Outcome |
|---|---|---|
| I | **Automation**: the WFS-FEM is a living model | A documented workflow keeps the model current with red tide imagery and in situ data (monthly, with on-demand updates during events) |
| II | **Integration**: outputs are used for decision-making | WFS-FEM products are delivered to SEDAR assessments, the Gulf SSC and NOAA IEA on their calendars and in their formats |
| III | **Communication**: modeling and findings are documented, visualized, understood and replicable | Versioned code and model releases, the redtideVIS visualizer, extension articles and peer-reviewed papers |

## Repository map

| Repository | Contents |
|---|---|
| [WFS-FEM/Ops](https://github.com/WFS-FEM/Ops) | This repository: plan, blueprint, decisions, risk register, meeting notes |
| [WFS-FEM/RedTideMaps](https://github.com/WFS-FEM/RedTideMaps) | Monthly red tide layer: FWC HAB cell counts, sdmTMB fits, satellite clipping, Ecospace ASCII drivers |
| [WFS-FEM/GFISHER](https://github.com/WFS-FEM/GFISHER) | Processing of GFISHER habitat and fish data |
| [WFS-FEM/EcospaceBasemap](https://github.com/WFS-FEM/EcospaceBasemap) | Static layers for the Ecospace basemap |
| WFS-FEM/EnvironmentalDrivers2EwE (private) | Environmental driver time series and maps formatted for EwE |
| WFS-FEM/Survey2EwE (private) | Survey-based abundance and distribution inputs formatted for EwE |
| WFS-FEM/SS2EwE (private) | Extraction of Stock Synthesis outputs as EwE inputs |
| WFS-FEM/diet (private) | Diet data used to parameterize the model |
| [dchagaris/R4EwE](https://github.com/dchagaris/R4EwE) | R package that drives the EwE software from R (general to EwE; also serves other models) |

The one-line descriptions of the private repositories are inferred from their names; correct them as needed.

## How the project board is used

- Every piece of work is an issue in the most relevant repository. Issues in this repository are added to the project automatically; issues in the code repositories are added from the issue sidebar.
- Each issue carries the project fields **Objective** (I, II, III or PM), **Stakeholder group** (A to H, multi-select), **Product** (A to H, multi-select), **Priority** (P0 to P3), **Phase** (the calendar quarter in which the item is expected to finish), **Target date**, **Lead** (Dave, Holden or Other) and, where relevant, **External partner(s)**. Product, Stakeholder group and Lead are the ones to set on every issue. Dated deliverables are **milestones** (M1 to M11) in this repository.
- Views: *Board* for daily work, *By objective* for planning, *Roadmap* for the timeline to September 2028, *Products* for stakeholder deliverables, *This quarter* for the quarterly check-in, *By lead* for Holden's and Dave's to-do lists, and *Decisions* for open decisions.
- Labels describe the kind of work (meeting, code, EwE, pipeline, docs, outreach, paper, decision, blocked); the fields carry the plan structure.
- Decisions are recorded in the issue that raised them and summarized in [`docs/decisions.md`](docs/decisions.md). Risks are tracked in [`docs/risk-register.md`](docs/risk-register.md); a risk that needs action becomes a task issue.
- Use the issue templates (task, meeting, decision) when opening issues here, then set the project fields in the issue sidebar.

## Documents

- [`docs/operationalization-plan.md`](docs/operationalization-plan.md): the one-page plan (vision statement)
- [`docs/project-blueprint.md`](docs/project-blueprint.md): how the project is structured and why, milestones, and the initial backlog
- [`docs/decisions.md`](docs/decisions.md): decision log
- [`docs/risk-register.md`](docs/risk-register.md): risk register

## Funding and partners

This work is part of the NOAA RESTORE Science Program award "Operationalizing the West Florida Shelf ecosystem model and application to red tides, stock assessment, and catch advice for Gulf reef fish" (University of Florida, with co-investigators at USF, FSU and Rice; October 2023 to September 2028). Named end users include the Gulf of Mexico Fishery Management Council and NOAA SERO.

## Key references

- Vilas, D. et al. (2023). Red tide effects on the West Florida Shelf evaluated via a spatially explicit ecosystem model. *Scientific Reports* 13:2541. https://doi.org/10.1038/s41598-023-29327-z
- Chagaris, D. (2025). Estimates of red tide mortality on red grouper 2002 to 2022 from the West Florida Shelf Fisheries Ecosystem Model. SEDAR 88 working paper.
- Sagarese, S. et al. (2026). Accounting for episodic mortality events in the estimation of fishery reference points for groupers in the Gulf of America. SEDAR105-WP-09.
- Moller, M. et al. (2026). Evaluating the risks of misspecifying red tide mortality within Gulf grouper stock assessments. SEDAR105-WP-12.
- Turley, B. et al. (2026). Garden of forking paths: EBFM and Florida red tides. *Reviews in Fish Biology and Fisheries* 36:48. https://doi.org/10.1007/s11160-026-10052-5
- Yao, Y., Hu, C. et al. (2026). How have Florida red tides changed? *Remote Sensing of Environment* 337:115345. https://doi.org/10.1016/j.rse.2026.115345
