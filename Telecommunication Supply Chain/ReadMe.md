# Overview
This assignment applied data wrangling and visualization skills to a policy-relevant research question in international trade. The goal was to combine multiple real-world datasets, produce publication-quality figures in R, and interpret findings in a short analytical paper using Quarto.

### Research Topic
The analysis examines how the U.S. position in the global telecommunications economy has changed from 2000 to 2022. Rather than relying solely on gross trade statistics, the paper compares surface-level import and export flows with domestic value-added (DVA) data to assess whether U.S. participation in telecommunications trade reflects genuine domestic productive capacity or growing dependence on foreign production networks — particularly those centered on China.

The central argument is that gross trade data and value-added data tell related but importantly different stories: the United States remains a major market and exporter, but its domestic value-added share has declined structurally, pointing to weakened productive capacity relative to global competitors.

| Dataset     | Description                                                                                                           | Source                                                   |
| ----------- | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| UN Comtrade | Gross U.S. telecommunications imports by partner country (2000–2022) and gross U.S. exports to the world              | https://comtradeplus.un.org/                             |
| OECD TiVA   | Domestic value added in U.S. final demand for telecommunications; domestic value added embodied in U.S. gross exports | https://www.oecd.org/en/topics/trade-in-value-added.html |

Comtrade commodity scope: Telecommunications equipment (HS chapters covering telephone sets, transmission apparatus, and related equipment)

TiVA industry scope: ICT / Telecommunications sector (ISIC Rev. 4 classification)

Time coverage: 2000–2022

### Approach
The analysis proceeds in four steps, each corresponding to a figure:

Figure 1 — U.S. imports from top source countries (2000–2022): A multi-line time series using UN Comtrade data, showing the rise of China as a dominant supplier and the subsequent shift toward Vietnam and Mexico in later years.

Figure 2 — Domestic value-added share in U.S. final demand: A single-line time series from OECD TiVA, constructed by dividing U.S. domestic value added by total value added in U.S. final telecommunications demand.

Figure 3 — U.S. gross telecommunications exports to the world: A line chart of total gross export values from UN Comtrade, providing the denominator context for Figure 4.

Figure 4 — Domestic value added in U.S. gross exports: A line chart of DVA from OECD TiVA, showing that DVA growth lags gross export growth — indicating rising foreign content in U.S. exports.

All figures were produced in R using ggplot2, dplyr, readr, and scales. Data cleaning steps include type coercion, exclusion of aggregate rows (e.g., "World", "Other Asia, NES"), and reshaping for join operations.

### References
Organisation for Economic Co-operation and Development (OECD). Trade in Value Added (TiVA) database. https://www.oecd.org/en/topics/trade-in-value-added.html

United Nations Comtrade Database. https://comtradeplus.un.org/
