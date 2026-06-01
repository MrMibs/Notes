
| Function      | Meaning           |                                                                                 |
| ------------- | ----------------- | ------------------------------------------------------------------------------- |
| `filter()`    | Keep rows         | filter(karse2, (growth > 0 \| humidity < 100)) <br>keep only growth > 0         |
| `select()`    | Keep columns      | df %>%   select(country, year, lifeExp)<br>Keep only those                      |
| `mutate()`    | Create columns    | df %>%  mutate(lifeExp_decade = lifeExp / 10)<br>New column with lifeExp_decade |
| `arrange()`   | Sort rows         | df %>%   arrange(desc(lifeExp))<br>Order lifeExp high to lov                    |
| `summarise()` | Compute summaries | df %>%   summarise(mean_lifeExp = mean(lifeExp))<br>does operations on a column |
| `group_by()`  | Work by groups    | df %>% group_by(continent) %>% summarise(above)<br>groups effects by continent  |
e.g.
students %>%
  filter(grade > 10) %>%
  arrange(desc(grade))

Take students → keep grades above 10 → sort descending.


data %>%
  filter(country == "Denmark") %>%
  group_by(year) %>%
  summarise(mean_value = mean(value)) %>%
  ggplot(aes(year, mean_value)) +
  geom_line()

We love %>% for feeding variables for no apparent reason, e.g.
d %>% as.data.frame() %>% head(n=10)


Filter for growth < 0 or hum > 100
a. filter(karse2, !(growth < 0 | humidity > 100))  VALID AND CORRECT
b. filter(karse2, growth >= 0) %>% filter(humidity < 100)  VALID AND CORRECT
c. filter(karse2, growth >= 0, humidity < 100)  VALID AND CORRECT
d. filter(karse2, growth >= 0 & humidity < 100)  VALID AND CORRECT
e. filter(karse2, growth >= 0 + humidity < 100)  INVALID
f. filter(karse2, growth >= 0 & humidity > 100)  FAULTY ">"
g. filter(karse2, !(growth >= 0)) %>% filter(humidity < 100) FAULTY "!"  
h. filter(karse2, !(growth < 0 & humidity > 100)) FAULTY "!"