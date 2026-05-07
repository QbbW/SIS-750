# Exemplary Code Chunk

### A reusable custom ggplot2 theme

One pattern I find useful when producing multi-figure reports is defining a custom `ggplot2` theme function once in a setup chunk, then calling it on every plot. This keeps all figures visually consistent without repeating theme code, and makes it easy to update the look of the entire report by changing one place.

The chunk below defines `theme_report()`, a lightweight wrapper around `theme_minimal()` that standardizes font sizes, bold axis titles and legend headings, a bottom-positioned legend, and a muted caption style. It also establishes a named color palette (`country_colors`) so that the same country always maps to the same color across all figures.

```r
# Visual style ---------------------------------------------------------------
main_blue   <- "#1874CD"
china_red   <- "#E63946"
muted_grey  <- "gray65"

country_colors <- c(
  "China"                      = "#E63946",
  "China (People's Republic of)" = "#E63946",
  "United States"              = "#1874CD",
  "USA"                        = "#1874CD",
  "Canada"                     = "#F4A261",
  "Mexico"                     = "#FFB6C1",
  "Japan"                      = "#6A4C93",
  "Rep. of Korea"              = "#E9C46A",
  "Korea"                      = "#E9C46A",
  "Viet Nam"                   = "#264653",
  "Thailand"                   = "#00247D",
  "India"                      = "#2A9D8F",
  "Chinese Taipei"             = "#7D26CD",
  "Taipei"                     = "#7D26CD",
  "EU28"                       = "#CD9B9B"
)

theme_report <- function(base_size = 12) {
  theme_minimal(base_size = base_size) +
    theme(
      plot.title    = element_text(face = "bold", size = base_size + 2, hjust = 0),
      plot.subtitle = element_text(size = base_size, color = "gray30", hjust = 0),
      plot.caption  = element_text(size = base_size - 2, color = "gray40", hjust = 1),
      legend.position  = "bottom",
      legend.title     = element_text(face = "bold"),
      panel.grid.minor = element_blank(),
      axis.title       = element_text(face = "bold"),
      strip.text       = element_text(face = "bold")
    )
}
```

**Example output** — applying `theme_report()` to Figure 1 (U.S. telecom imports by source country):

```r
ggplot(plot_data, aes(x = refYear, y = primaryValue,
                      color = partnerDesc, group = partnerDesc)) +
  geom_line(linewidth = 1) +
  scale_color_manual(values = country_colors) +
  scale_y_continuous(labels = label_number(scale_cut = cut_short_scale())) +
  labs(
    title   = "U.S. Imports from Top Source Countries",
    caption = "Source: UN Comtrade",
    x = "Year", y = "Import Value (USD)", color = "Country"
  ) +
  theme_report()
```



> The same `theme_report()` call is appended to every figure in the report, ensuring a uniform visual language across all eight charts without duplicating any styling code.
