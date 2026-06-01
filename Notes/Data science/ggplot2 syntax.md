ggplot(aes(), data =) + geom_point

This means everything has to go into either data, aes or points / lines.

aes arguments:

| Aesthetic | Meaning          | Example               |
| --------- | ---------------- | --------------------- |
| x         | x-axis           | aes(x = year)         |
| y         | y-axis           | aes(y = value)        |
| color     | line/point color | aes(color = group)    |
| fill      | fill color       | aes(fill = group)     |
| size      | point/line size  | aes(size = weight)    |
| shape     | point shape      | aes(shape = species)  |
| alpha     | transparency     | aes(alpha = group)    |
| linetype  | line style       | aes(linetype = group) |
| group     | grouping         | aes(group = id)       |
Unnamed arguments work for aes() as it can guess arguments xlab ylab but after it is clueless. Further it expects
ggplot(data,aes) if data= is not used.

Further

|Variable (data)|Can be mapped to|Requirements / constraints|
|---|---|---|
|`light`|`color`, `size`, `alpha`|numeric (continuous) or factor (categorical) depending on mapping|
|`temperature`|`x`, `y`, `color`, `size`, `alpha`|numeric preferred for axes, continuous or factor allowed for aesthetics|
|`humidity`|`x`, `y`, `color`, `size`, `alpha`|numeric or factor (continuous better for scaling aesthetics)|
|`distance`|`x`, `y`, `size`, `color`, `alpha`|numeric required for meaningful scaling|
|`time`|`x`, `y`, `group`, `color`|numeric, date/time, or ordered factor|
|`group/id`|`color`, `shape`, `linetype`, `group`|must be categorical (factor/character)|
|categorical labels (e.g. treatment, species)|`color`, `fill`, `shape`, `linetype`|should have limited number of levels (< ~6–8 for shapes)|
|continuous measurements (e.g. weight, intensity)|`color`, `size`, `alpha`|numeric only (needed for gradients/scaling)|

After the + you can add

|Component|What it does|Example|
|---|---|---|
|`geom_point()`|scatterplot (points)|`+ geom_point()`|
|`geom_line()`|line plot|`+ geom_line()`|
|`geom_bar()`|bar chart (counts)|`+ geom_bar()`|
|`geom_col()`|bar chart (precomputed values)|`+ geom_col()`|
|`geom_histogram()`|histogram|`+ geom_histogram()`|
|`geom_boxplot()`|boxplot|`+ geom_boxplot()`|
|`stat_smooth()`|adds trend line (regression/loess)|`+ stat_smooth()`|
|`labs()`|titles and axis labels|`+ labs(title = "...")`|
|`theme_minimal()`|clean visual theme|`+ theme_minimal()`|
|`theme_bw()`|black/white theme|`+ theme_bw()`|
|`facet_wrap()`|split plot by variable|`+ facet_wrap(~group)`|
|`facet_grid()`|split plot in grid form|`+ facet_grid(a ~ b)`|
|`scale_x_continuous()`|control x-axis scaling|`+ scale_x_continuous()`|
|`scale_y_continuous()`|control y-axis scaling|`+ scale_y_continuous()`|
|`scale_color_manual()`|manually set colors|`+ scale_color_manual()`|
|`coord_flip()`|flips x and y axes|`+ coord_flip()`|

![[Facet_wrap]]

![[Geom]]


![[scale_x_continuous + scale_color_binned]]

[[Example]]
[[Functions in ggplot framework]]