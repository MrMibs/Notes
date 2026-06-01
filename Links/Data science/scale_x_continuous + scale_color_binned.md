#datascience
ggplot(...) +
  geom_point() +
  scale_x_continuous(limits = c(0, 1.2)) +
  scale_y_continuous(limits = c(0, 100)) +
  scale_color_binned(type = "viridis") +
  theme_classic()

**`scale_*_continuous()`** = keeps values **smooth and numeric (continuous mapping)** **`scale_*_binned()`** = turns continuous values into **groups (bins) first, then colors/scales those groups**


