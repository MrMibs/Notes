ggplot(dw, aes(x = delta_time, y = growth, color = temperature)) +
  geom_point(size = 5, alpha = 0.1) +
  geom_smooth(
    data = du_subset,
    method = "lm",
    color = "red",
    linewidth = 2,
    se = FALSE
  ) +
  labs(x = "Dage", y = "Vekst [cm]") +
  scale_color_binned(type = "viridis") +
  theme(
    axis.text = element_text(color = "darkgrey"),
    axis.text.x = element_text(angle = 0),
    axis.line = element_line(),
    panel.background = element_rect(fill = "grey95"),
    legend.position = c(0.1, 0.9),
    legend.background = element_blank()
  )