# Risk register

Reviewed at each quarterly re-plan. Likelihood and impact are rated Low, Medium or High. Risks that need action are turned into task issues; the Issue column links to them.

| # | Risk | Likelihood | Impact | Mitigation | Owner | Issue |
|---|---|---|---|---|---|---|
| R1 | Satellite continuity: MODIS Aqua nFLH ends; VIIRS rasters are obtained by hand and stop at 2024-12 in RedTideMaps | High | High | Build an automated VIIRS feed with the Hu lab; document and test the buffered-hull fallback around in situ positives | | |
| R2 | Windows and EwE console dependency: automated runs need a Windows host | Medium | Medium | Provision a scheduled task or self-hosted runner; document setup | | |
| R3 | Single-person knowledge: the pipeline currently runs only on one person's machine with hard-coded paths | High | High | Config file, written runbook, second-person end-to-end run (milestone M2) | | |
| R4 | GFISHER geodatabase not public: limits replicability of the basemap | Medium | Medium | Decide on public access or a documented access path | | |
| R5 | Calibration does not improve fits: Ecospace calibration attempted for SEDAR 88 gave no noticeably better fits | Medium | High | Calibration and validation milestone with explicit acceptance criteria; report honestly if not met | | |
| R6 | Credibility with assessment analysts: past difficulty using external red tide magnitude estimates directly in assessments (SEDAR 88); Ecospace index and LEK disagree for 2014 and 2018 | Medium | High | Validation and reconciliation track (surveys, LEK, hypoxia); deliverables agreed with analysts up front | | |
| R7 | Funding ends September 2028 before RL 9 is reached | Medium | High | Anchor milestones to award end; identify a maintenance home for the monthly workflow | | |

Sources: Vilas et al. (2023); Chagaris (2025, SEDAR 88 WP); Sagarese et al. (2026, SEDAR105-WP-09); Moller et al. (2026, SEDAR105-WP-12); Turley et al. (2026); WFS-FEM/RedTideMaps repository; NASA Aqua mission status page.
