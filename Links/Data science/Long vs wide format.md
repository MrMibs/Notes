# LONG
| country     | continent | year | variable  | value   |
| ----------- | --------- | ---- | --------- | ------- |
| Afghanistan | Asia      | 1952 | lifeExp   | 28.8    |
| Afghanistan | Asia      | 1952 | pop       | 8425333 |
| Afghanistan | Asia      | 1952 | gdpPercap | 779     |
| Afghanistan | Asia      | 1957 | lifeExp   | 30.3    |
| Afghanistan | Asia      | 1957 | pop       | 9240934 |

![[Pasted image 20260530111724.png]]


5,112 × 5 table

1 fff <- ggg %>% pivot_longer(
2    cols = c(lifeExp, pop, gdpPercap),
3    names_to = "variable",
4    values_to = "value"
5  )

1 pivot longer
2 Selects colums lifeExp, pop and gdpPercap or lifeExp:gdpPercap
3 Stores column names as variable
4 Stores column values as variable values

**Long format** → used for analysis, plotting (especially ggplot2), and most tidyverse workflows

---

# WIDE

| country     | continent | year | lifeExp | pop      | gdpPercap |
| ----------- | --------- | ---- | ------- | -------- | --------- |
| Afghanistan | Asia      | 1952 | 28.8    | 8425333  | 779       |
| Afghanistan | Asia      | 1957 | 30.3    | 9240934  | 821       |
| Afghanistan | Asia      | 1962 | 32.0    | 10267083 | 853       |
| Afghanistan | Asia      | 1967 | 34.0    | 11537966 | 836       |
| Afghanistan | Asia      | 1972 | 36.1    | 13079460 | 740       |

![[Pasted image 20260530111413.png]]

1,704 × 6 table

ggg <- fff %>%
  pivot_wider(
    names_from = variable,
    values_from = value
  )


1 pivot wider
2 columns from variable
3 values from values

**Wide format** → used for tables, reporting, and some models that expect variables in separate columns
