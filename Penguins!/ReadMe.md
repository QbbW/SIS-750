# Exploratory Visualization with Palmer Penguins
Assignment Overview
This assignment introduced core data visualization workflows in R using ggplot2. The goal was to explore a real world dataset through multiple chart types, practice layering geoms, and communicate findings through visual storytelling.

Research Topic
The analysis examines morphological variation across three penguin species — Adelie, Chinstrap, and Gentoo — in the Palmer Archipelago, Antarctica. Specifically, the visualizations investigate relationships between bill dimensions, flipper length, body mass, and sex, as well as the geographic distribution of species across islands.

Data
Dataset: palmerpenguins R package
Source: https://allisonhorst.github.io/palmerpenguins/
Original data collected by: Dr. Kristen Gorman and the Palmer Station Long Term Ecological Research (LTER) Program

Approach
1. Bill length vs bill depth by species: a scatterplot using color to distinguish species, revealing a Simpson's Paradox-like pattern where the three species form distinct clusters.
2. Body mass and Sex and Species: a scatterplot with per-species OLS regression lines (geom_smooth(method = "lm")), showing a positive within-species relationship and clear interspecies differences.
3. Flipper length vs. body mass by species: a layered boxplot overlaid with group mean points and connecting lines, using position_dodge for alignment and a merged fill/color legend.
4. Bill length vs. flipper length faceted by island: a faceted scatterplot (facet_wrap(~ island)) revealing that Adelie penguins inhabit all three islands, while Gentoo and Chinstrap are each restricted to one island.

Files
Penguins.qmd: Quarto script with all code and narrative
Penguins.pdf: Rendered PDF output
