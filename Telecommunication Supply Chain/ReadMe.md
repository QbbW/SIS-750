# Seeing Through Gross Trade: U.S. Telecommunications, Value Added, and Chinese Supply-Chain Exposure
### What this is
This report asks a simple but analytically tricky question: when the United States buys and sells telecommunications goods, how much of the underlying value is actually made in America — and how much is Chinese? Gross trade data (who ships what to whom) can't answer that on its own. This project combines three datasets to dig deeper.

### Research question
Does the United States remain strong in telecommunications production, or do gross trade patterns conceal deeper dependence on foreign and Chinese value added?

| Dataset     | Description                                                                                                           | Source                                                   |
| ----------- | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| UN Comtrade | Gross U.S. telecommunications imports by partner country (2000–2022) and gross U.S. exports to the world              | https://comtradeplus.un.org/                             |
| OECD TiVA   | Domestic value added in U.S. final demand for telecommunications; domestic value added embodied in U.S. gross exports | https://www.oecd.org/en/topics/trade-in-value-added.html |

Comtrade commodity scope: Telecommunications equipment (HS chapters covering telephone sets, transmission apparatus, and related equipment)

TiVA industry scope: ICT / Telecommunications sector (ISIC Rev. 4 classification)

Time coverage: 2000–2022

### Approach
The analysis builds in three layers:

Gross trade (UN Comtrade) — who the U.S. directly imports from and exports to, and how that geography has shifted since 2000

Value-added (OECD TiVA) — how much of the value in U.S. telecom final demand and exports is actually created domestically vs. abroad

Chinese value added (ADB MRIO) — how much Chinese-origin value reaches U.S. supply chains, including indirectly through third countries like Vietnam, Mexico, and Korea

Eight figures are produced in total, moving from surface-level trade flows to deeper production-network exposure.

### References
Organisation for Economic Co-operation and Development (OECD). Trade in Value Added (TiVA) database. https://www.oecd.org/en/topics/trade-in-value-added.html

United Nations Comtrade Database. https://comtradeplus.un.org/
