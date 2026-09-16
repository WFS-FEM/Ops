# WFS-FEM Operationalization Plan

*One-page vision statement. Version of September 2026, with notes from the meeting with Dave Chagaris. The Word original is kept in the shared UF folder "WFS Fisheries Ecosystem Modeling/operationalizing".*

**Operational = Automated + Integrated + Communicated**

## Objectives

**I. Automation: the WFS-FEM is a "living model."**
Create a workflow for data processing and model simulations that keeps the model current with red tide imagery and in situ observations (monthly, with on-demand updates during events).

**II. Integration: outputs are used for decision-making.**
Facilitate the use of WFS-FEM outputs to inform stock assessments and reference points.

**III. Communication: modeling and findings are documented, visualized, understood, and able to be replicated.**
Data, assumptions, modeling, and results are carefully documented and communicated to key stakeholder groups, including assessment scientists, fisheries managers, and fishers.

## Key stakeholder groups and products

**A. SEDAR stock assessments**: red tide mortality (M<sub>rt</sub>) estimates and accompanying documentation.
Gulf assessment group: Katie Siegfried, Skyler Sagarese, Lisa Ailloud, Shanae Allen.
To do: schedule a meeting with the assessment team and ask for feedback on products, including an R Shiny app with automated markdown summaries (by species) that feed data inputs and the ability to download data; animations; spatial data (netCDF).

**B. NOAA Integrated Ecosystem Assessment (IEA) and ecosystem status reports.**
To do: schedule a meeting with Mandy Karnauskas, Matt McPherson, Chris Kelble and Brendan Turley on satellite products, biogeochemical products (hypoxia, assuming the model works), and synthetic ecosystem-model outputs or ecological indicators. Identify individual contacts.

**C. Fisheries managers and fishers**: Ryan Rindone, John Froeschke, NOAA SERO, Mike Allen, CJ Sweetman (Gulf Council, FWC).
Products: an interactive visualizer (R Shiny) website, updating https://redtidevis.shinyapps.io/redtideapp/; extension and outreach articles (one-pagers, EDIS).

**D. Ecosystem modelers and the research community.**
Products: the GitHub organization https://github.com/WFS-FEM; the R package R4EwE https://github.com/dchagaris/R4EwE; usage vignettes.

**E. Broader research community**: peer-reviewed research article(s).

## To-dos

- Stakeholder meetings (fall 2026)

## Notes on wording

- "WFS-FEM" is the project's form of the acronym (decision of 9 September 2026).
- The SEDAR product is a red tide mortality (M<sub>rt</sub>) index, not natural mortality (M).
- The model is a nowcast with a lag plus scenario projections; operational *K. brevis* forecasts extend only 3 to 4 days (Sagarese et al. 2026, SEDAR105-WP-09), so "monthly, with on-demand updates during events" is the supportable cadence.
