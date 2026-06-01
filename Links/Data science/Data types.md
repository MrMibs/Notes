# Common Arduino Data Types

| Type | Example | Typical Use |
|--------|---------|---------|
| `int` | `int count = 42;` | General whole numbers |
| `unsigned int` | `unsigned int rpm = 1500;` | Non-negative counts |
| `long` | `long time = millis();` | Large integers, timestamps |
| `unsigned long` | `unsigned long startTime;` | `millis()`, timers |
| `float` | `float voltage = 3.3;` | Decimal numbers |
| `double` | `double x = 3.14;` | Same as `float` on most Arduinos |
| `char` | `char letter = 'A';` | Single characters |
| `char[]` | `char name[] = "Pump";` | Text strings (C-style) |
| `String` | `String msg = "Hello";` | Easier text handling |
| `bool` | `bool running = true;` | True/False values |
| `byte` | `byte sensor = 255;` | Small integers (0–255) |

# Common R data types

| Type | Meaning        | Example            | Typical Use                            |
| ---- | -------------- | ------------------ | -------------------------------------- |
| dbl  | Double (float) | 3.14               | Measurements, concentrations, ages     |
| int  | Integer        | 5                  | Counts, number of deaths, observations |
| chr  | String         | "Denmark"          | Names, IDs, labels                     |
| lgl  | Logical        | TRUE               | Filtering and conditions               |
| fct  | Factor         | Control, Treatment | Categorical variables                  |
| date | Date           | 2026-06-15         | Time series data                       |
| dttm | Datetime       | 2026-06-15 14:30   | Timestamped measurements               |
