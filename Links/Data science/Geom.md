# Geom

| Geom               | What it draws         | Required aesthetics | Common optional aesthetics           |
| ------------------ | --------------------- | ------------------- | ------------------------------------ |
| `geom_point()`     | points (scatterplot)  | `x`, `y`            | `color`, `size`, `shape`, `alpha`    |
| `geom_line()`      | connected lines       | `x`, `y`            | `color`, `linetype`, `size`, `group` |
| `geom_bar()`       | bar chart (counts)    | `x`                 | `fill`, `color`                      |
| `geom_col()`       | bar chart (values)    | `x`, `y`            | `fill`, `color`                      |
| `geom_histogram()` | distribution bars     | `x`                 | `fill`, `color`, `bins` (argument)   |
| `geom_boxplot()`   | box-and-whisker plot  | `x`, `y`            | `fill`, `color`, `alpha`             |
| `geom_smooth()`    | trend/regression line | `x`, `y`            | `color`, `linetype`, `method`        |
| `geom_jitter()`    | jittered points       | `x`, `y`            | `color`, `size`, `alpha`             |
| `geom_text()`      | text labels           | `x`, `y`, `label`   | `color`, `size`, `angle`             |
| `geom_density()`   | density curve         | `x`                 | `color`, `fill`, `alpha`             |
