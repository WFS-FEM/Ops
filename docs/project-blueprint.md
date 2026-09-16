# WFS-FEM Operationalization: GitHub Project blueprint

Draft 3, 14 September 2026. Holden's revision of 14 September with mechanical corrections applied (milestone renumbering, product-letter remap, label and cross-reference fixes) and decisions of 14 September (M2 due 2026-12-31; Phase single select). Sources: the Operationalization Plan one-pager (with notes from the meeting with Dave Chagaris), the plan review of 9 September 2026, the NOAA RESTORE proposal and milestone chart, and the current state of the WFS-FEM and dchagaris/R4EwE repositories.

**Build status (15 September 2026):** built as described below at https://github.com/orgs/WFS-FEM/projects/4. Issues #1 to #21 in WFS-FEM/Ops match the backlog numbering in section 8, with all project fields, milestones and labels set. Views 2, 4 and 6 group by Objective, Product and Lead respectively (grouping by a multi-select field works). The Roadmap view uses Target date, which is still blank on every item; set it when dates firm up after the fall meetings.

## 1. Purpose and design choices

The GitHub Project is the working plan to take the West Florida Shelf Fisheries Ecosystem Model (WFS-FEM) from a demonstrated prototype (roughly NOAA readiness level 7 under NAO 216-105B) to a tool used routinely (RL 9) by the end of the NOAA RESTORE award in September 2028. The one-page plan remains the vision statement; this project turns the vision into dated, owned tasks. The tasks are primarily Holden's to-dos; the framework lets Dave (and others) add and assign tasks too.

Design choices, with reasons:

- **Organization-level project** (owner: WFS-FEM), not a repository project. Work spans Ops, RedTideMaps, GFISHER, EcospaceBasemap and dchagaris/R4EwE. An organization project can hold issues from any of those repositories, whereas milestones and labels are per repository. The Ops repository is the planning home: cross-cutting issues, meetings, documents, and decisions live there.
- **Project custom fields carry the plan's structure** (Objective, Stakeholder group, Product, Priority, Phase, Lead). These are cross-repository, so an issue filed in RedTideMaps can be tagged "Objective I" without RedTideMaps needing matching labels.
- **Products are the main organizing axis.** Most work is organized around the eight products (A to H), so Product is set on every issue and the Products view is the stakeholder-facing view.
- **Milestones live in Ops** and mark dated deliverables. They appear as markers on the roadmap view.
- **Labels stay small** and describe the kind of work, not the plan structure (the fields do that).
- **Dates through Sept 2028 are provisional.** Near-term items (2026 Q4 to 2027 Q2) are specific; later items are placeholders to be re-planned each quarter and re-anchored once the 2027 to 2028 SEDAR schedule is confirmed with SEFSC.

## 2. Project settings

| Setting | Value |
|---|---|
| Owner | WFS-FEM (organization) |
| Title | WFS-FEM Operationalization |
| Short description | Operational = Automated + Integrated + Communicated. Work plan to make the WFS-FEM a routinely used tool by Sept 2028 (NOAA RESTORE award end). |
| Visibility | Public |
| Linked repositories | WFS-FEM/Ops, WFS-FEM/RedTideMaps, WFS-FEM/GFISHER, WFS-FEM/EcospaceBasemap. An organization project can only be linked to repositories owned by the organization, so dchagaris/R4EwE cannot be linked while it lives under Dave's account; its issues can still be added to the project one at a time, or the repository can be transferred to WFS-FEM (Dave's call). |
| README | Points to this blueprint and the one-page plan |

## 3. Fields

Built-in fields kept: Title, Assignees, Status, Labels, Milestone, Repository, Linked pull requests.

**Status** (single select, edit the defaults): Backlog, Ready, In progress, Blocked, In review, Done.

Custom fields:

| Field | Type | Options / notes |
|---|---|---|
| Objective | Single select | I. Automation; II. Integration; III. Communication; PM (project management) |
| Stakeholder group | Multi-select (public preview since July 2026) | A. SEFSC Gulf Fisheries Branch / SEDAR; B. Gulf IEA / ESR; C. Fisheries managers; D. Ecosystem modelers; E. Science community; F. Fishers and public; G. Funder (NOAA RESTORE reporting); H. Other |
| Product | Multi-select (public preview) | A. EwE model update; B. SEDAR Mrt; C. Shiny App; D. R package; E. IEA/ESR; F. Peer-reviewed paper; G. Report; H. Other |
| Priority | Single select | P0 critical path; P1 high; P2 normal; P3 nice to have |
| Phase | Single select (see note) | 2026 Q4; 2027 Q1; 2027 Q2; 2027 Q3; 2027 Q4; 2028 Q1; 2028 Q2; 2028 Q3; Beyond award |
| Target date | Date | Drives the roadmap layout |
| Lead | Single select | Dave; Holden; Other |
| External partner(s) | Text | External partner(s) for the item |

Eight custom fields. Product, Stakeholder group and Lead are the three that matter most for filtering and should be set on every issue.

Note on Phase: a task that spans quarters is better expressed by Target date (and, on the roadmap, a start and end date) than by ticking several quarters, and "This quarter" filtering only works cleanly with one value per item. Phase is therefore single select, meaning the quarter in which the item is expected to finish. If a true "current quarter" filter is wanted, an Iteration field with 13-week iterations is the alternative.

Note on multi-select fields: GitHub's changelog confirms filtering by them in views, and when the project was built (September 2026) the table layout also offered "group by" for the multi-select Product field, so the Products view groups by Product; "slice by Product" remains an alternative.

## 4. Views

| # | View | Layout | Configuration | Used for |
|---|---|---|---|---|
| 1 | Board | Board | Columns = Status | Day-to-day work |
| 2 | By objective | Table | Group by Objective; sort by Priority, then Target date; show Product, Stakeholder group, Phase, Milestone, Lead | Planning conversations with Dave |
| 3 | Roadmap | Roadmap | Date field = Target date; group by Objective; milestone markers on; zoom = quarter | Timeline to Sept 2028 |
| 4 | Products | Table | Group (or slice) by Product; show Stakeholder group, Status, Phase, Milestone, Lead | Stakeholder-facing deliverables |
| 5 | This quarter | Table | Filter Phase = current quarter; group by Status | Quarterly check-in |
| 6 | By lead | Table | Group by Lead; filter Status is not Done; sort by Target date | Holden's and Dave's to-do lists |
| 7 | Decisions | Table | Filter label:decision; show External partner(s) | Open decisions |

## 5. Built-in workflows

| Workflow | Setting |
|---|---|
| Item added to project | Status = Backlog |
| Item reopened | Status = Backlog |
| Item closed | Status = Done |
| Auto-add to project | Repository WFS-FEM/Ops, filter `is:issue` (issues in other repositories are added by hand from the issue sidebar) |
| Auto-archive | Status = Done and last updated more than 90 days ago |

## 6. Labels (Ops repository; copy to the code repositories as needed)

| Label | Colour | Meaning |
|---|---|---|
| meeting | #0E8A16 | Schedule or hold a meeting |
| code | #1D76DB | Software or workflow work |
| EwE | #008080 | Involves Ecopath with Ecosim and Ecospace runs |
| pipeline | #5319E7 | Involves linking different project efforts |
| docs | #FBCA04 | Documentation, plans, vignettes |
| outreach | #F9D0C4 | Extension, SSC, Council, fishers |
| paper | #C2E0C6 | Manuscripts and working papers |
| decision | #D93F0B | A decision is needed; record the outcome in the issue |
| blocked | #000000 | Waiting on someone or something outside the team |

## 7. Milestones (Ops repository; dates provisional)

| # | Milestone | Due | Success test |
|---|---|---|---|
| M1 | Fall 2026 stakeholder meetings | 2026-12-18 | Transition plan drafted; meetings scheduled; meetings held |
| M2 | Monthly pipeline reproducible | 2026-12-31 | Holden runs the monthly workflow end to end from documented instructions |
| M3 | SEDAR 105 (gag) red tide products delivered | 2026-11-30 (confirm TWG data deadline) | Mrt products delivered by the deadline |
| M4 | Automated monthly satellite feed operational | 2027-06-30 | Current-month VIIRS outputs are pulled and run in the model |
| M5 | Automated monthly BGC model feed operational | 2027-06-30 | Current-month BGC outputs are pulled and run in the model |
| M6 | R package (R4EwE v1.0) | 2027-06-30 | Tests, CI, pkgdown site, at least two usage vignettes, tagged release |
| M7 | Shiny App (redtideVIS v2) | 2027-09-30 | Updated redtideVIS with Mrt with uncertainty, data-currency stamp, data downloads |
| M8 | Shiny App (single species) | 2027-12-30 | Inputs and outputs can be viewed and downloaded by functional group |
| M9 | Full model | TBD | Full model updated with the full capabilities of the MICE model |
| M10 | ESR outputs | TBD | Products (red tide satellite, BGC outputs, synthetic EM outputs) routinely delivered for Gulf ESRs, coordinated with the NOAA Gulf IEA group |
| M11 | All products fully archived | 2028-09-30 | Model database, code and products archived with DOIs; final report |

## 8. Issue backlog

Columns: Objective (Obj), Stakeholder group (SG), Product (Prod), Priority (Pri), Phase, Milestone (MS), Labels, External partner(s). Lead is Holden unless stated. Bodies will carry context, acceptance criteria and the sources listed in section 9. Further issues will be created as products are designed with the stakeholder groups.

### Project management

| # | Title | Obj | SG | Prod | Pri | Phase | MS | Labels | External partner(s) |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Expand the one-page plan into a transition plan (scope, success criteria, timeline) | PM | G | G | P0 | 2026 Q4 | M1 | docs | |
| 2 | Trace the plan to the NOAA RESTORE award deliverables and named end users | PM | G | G | P1 | 2026 Q4 | M1 | docs | |
| 3 | Set up the Ops repository (README, issue templates, docs folder, this blueprint) | PM | D | H | P1 | 2026 Q4 | M1 | docs | |

### Objective I: Automation

| # | Title | Obj | SG | Prod | Pri | Phase | MS | Labels | External partner(s) |
|---|---|---|---|---|---|---|---|---|---|
| 4 | Build an automated satellite red tide feed with the Hu lab | I | D | A | P0 | 2027 Q2 | M4 | code, pipeline | Hu lab (USF) |
| 5 | Replace hard-coded paths in RedTideMaps `run_redtide_maps.R` with a config file and have a second person run it | I | D | A | P0 | 2026 Q4 | M2 | code | |
| 6 | Reconcile the RedTideMaps README and script header on whether the FWC HAB pull is automatic | I | D | A | P2 | 2026 Q4 | M2 | docs | |
| 7 | Create an orchestration workflow that runs the monthly pipeline end to end and logs each run | I | D | A | P0 | 2026 Q4 | M2 | code, pipeline, decision | |
| 8 | Extend the driver pipeline beyond red tide (e.g., DO, temperature, salinity, chlorophyll/NPP, effort) | I | D | A | P2 | 2027 Q3 | M9 | code, pipeline | |
| 9 | Integrate hypoxia and BGC drivers (contingent on model performance) | I | B, D | A, E | P2 | 2028 Q1 | M5 | EwE, pipeline | Stukel (FSU) |
| 10 | Version and archive the WFS-FEM model database as a tagged release with a DOI | I | D | A | P1 | 2027 Q2 | M11 | docs, EwE | |

### Objective II: Integration

| # | Title | Obj | SG | Prod | Pri | Phase | MS | Labels | External partner(s) |
|---|---|---|---|---|---|---|---|---|---|
| 11 | Stakeholder meeting: Gulf assessment group. Feedback on products: Shiny summaries by species, data download, animations, netCDF | II | A | B, C | P0 | 2026 Q4 | M1 | meeting | Siegfried, Sagarese, Ailloud, Allen (SEFSC) |
| 12 | Stakeholder meeting: Gulf IEA. How products could be incorporated into ESRs (satellite products, BGC outputs, synthetic EM outputs, ecological indicators) | II | B | E | P0 | 2026 Q4 | M1 | meeting | Karnauskas, McPherson, Turley |
| 13 | Stakeholder meeting: fisheries managers. Feedback on products: Shiny apps, extension articles, others | II | C | C, H | P0 | 2026 Q4 | M1 | meeting | Rindone, Froeschke (GMFMC); SERO; Allen; Sweetman (FWC) |
| 14 | Stakeholder meeting: fishers. Feedback on products: Shiny apps, extension articles, others | II | F | C, H | P0 | 2026 Q4 | M1 | meeting | Sipos (Sea Grant), Streeter (FCWC) |
| 15 | Finalize the deliverables table | II | A | B | P0 | 2026 Q4 | M1 | docs | |
| 16 | Support the SEDAR 105 (gag) Red Tide Mortality TWG and deliver requested Mrt products by the data deadline | II | A | B | P0 | 2026 Q4 | M3 | EwE | Gulf assessment team (Sagarese, Moller) |

### Objective III: Communication

| # | Title | Obj | SG | Prod | Pri | Phase | MS | Labels | External partner(s) |
|---|---|---|---|---|---|---|---|---|---|
| 17 | R4EwE: pkgdown site, restore the vignette as .Rmd, and write usage vignettes | III | D, E | D | P1 | 2027 Q2 | M6 | docs | Chagaris (Lead: Dave) |
| 18 | redtideVIS v2: current-month Mrt with uncertainty, data-currency stamp, summaries, downloads, animations, netCDF | III | A, C, F | C | P1 | 2027 Q3 | M7 | code | |
| 19 | Publish the redtideVIS app source in the WFS-FEM organization | III | D | C | P2 | 2027 Q1 | M7 | code | |
| 20 | Extension and outreach articles (EDIS one-pagers) | III | C, F | H | P2 | 2027 Q4 | M7 | outreach | |
| 21 | Peer-reviewed paper on operationalizing the WFS-FEM | III | E | F | P2 | 2028 Q2 | M11 | paper | |

## 9. Sources used for the backlog

- NOAA RESTORE proposal, "Operationalizing the West Florida Shelf ecosystem model and application to red tides, stock assessment, and catch advice for Gulf of Mexico reef fish" (LOI 021), narrative, data management plan, stakeholder engagement plan and milestone chart (revised May 2023). Project file.
- Vilas, D. et al. (2023). Red tide effects on the West Florida Shelf evaluated via a spatially explicit ecosystem model. Scientific Reports 13:2541. https://doi.org/10.1038/s41598-023-29327-z
- Chagaris, D. (2025). Estimates of red tide mortality on red grouper 2002 to 2022 from the West Florida Shelf Fisheries Ecosystem Model. SEDAR 88 working paper.
- Sagarese, S. et al. (2026). Accounting for episodic mortality events in the estimation of fishery reference points for groupers in the Gulf of America. SEDAR105-WP-09.
- Moller, M. et al. (2026). Evaluating the risks of misspecifying red tide mortality within Gulf grouper stock assessments. SEDAR105-WP-12.
- Turley, B. et al. (2026). Garden of forking paths: EBFM and Florida red tides. Reviews in Fish Biology and Fisheries 36:48. https://doi.org/10.1007/s11160-026-10052-5
- Yao, Y., Hu, C. et al. (2026). How have Florida red tides changed? Remote Sensing of Environment 337:115345. https://doi.org/10.1016/j.rse.2026.115345
- NOAA NAO 216-105B, Policy on research and development transitions (readiness levels). https://www.noaa.gov/organization/administration/nao-216-105b-policy-on-research-and-development-transitions
- NOAA RESTORE Science Program project page. https://restoreactscienceprogram.noaa.gov/projects/red-tide-and-reef-fish-modeling
- Federal Register notice for the SEDAR 105 Red Tide Mortality TWG meeting (8 Sept 2026). https://www.federalregister.gov/documents/2026/08/07/2026-16095/
- GitHub Docs, About Projects. https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects
- GitHub Changelog, Multi-select fields for Projects and Issues in public preview (23 July 2026). https://github.blog/changelog/2026-07-23-multi-select-fields-for-projects-and-issues-in-public-preview/
- Repositories: https://github.com/WFS-FEM (Ops, RedTideMaps, GFISHER, EcospaceBasemap); https://github.com/dchagaris/R4EwE

## 10. Working agreement (proposed)

- New work starts as an issue in the most relevant repository; every issue gets Objective, Product, Stakeholder group, Lead, Priority and Phase within a week of creation (the "By objective" view shows blanks).
- The Board is the daily view; "By lead" is each person's to-do list; the Roadmap is reviewed at each quarterly re-plan; "Decisions" is reviewed at every meeting with Dave.
- Decisions are recorded in the issue that raised them, then the `decision` label is removed and the outcome is summarized in `docs/decisions.md`.
- A product that goes to SEDAR or the SSC references a tagged release of the model database and of R4EwE (issue 10 sets the policy).
- The quarterly status update uses the project's built-in Status updates feature so the history is kept with the project.
