1. rsample   → split data (train/test, cross-validation)
2. recipes   → preprocess + feature engineering
3. parsnip   → define model (logistic regression, RF, etc.)
4. workflows → combine recipe + model
5. tune      → hyperparameter tuning (optional)
6. fit       → train final model
7. predict   → make predictions
8. yardstick → evaluate performance


## 🔧 Step-by-Step Description (Tidymodels)

### 1. rsample — Data Splitting
- Splits dataset into training and testing sets
- Creates cross-validation folds
- Ensures unbiased model evaluation

**Common functions:**
- `initial_split()`
- `training()`
- `testing()`
- `vfold_cv()`

---

### 2. recipes — Preprocessing
- Defines feature engineering steps before modeling
- Does not modify data immediately (declarative workflow)

**Typical tasks:**
- Normalization / scaling
- Dummy variable encoding
- Missing value imputation

**Common steps:**
- `step_normalize()`
- `step_dummy()`
- `step_impute_mean()`

---

### 3. parsnip — Model Specification
- Defines model type without fitting it
- Separates model type from computational engine

[[Models, engines, and modes]]

**Examples:**
- `linear_reg()`
- `logistic_reg()`
- `rand_forest()`

**Engines:**
- `"lm"` → linear models
- `"glmnet"` → regularized regression
- `"ranger"` → random forest

---

### 4. workflows — Combine Steps
- Combines recipe + model into one pipeline
- Prevents data leakage
- Makes workflow reproducible and structured

---

### 5. tune — Hyperparameter Tuning (Optional)
- Finds best model parameters
- Uses cross-validation

**Methods:**
- Grid search
- Random search

---

### 6. fit — Train Model
- Fits workflow/model to training data
- Produces trained model object

---

### 7. predict — Make Predictions
- Applies trained model to new data

**Outputs:**
- Numeric values (regression)
- Class labels or probabilities (classification)

---

### 8. yardstick — Model Evaluation
- Evaluates model performance

**Regression metrics:**
- `rmse`
- `mae`
- `rsq`

**Classification metrics:**
- `accuracy`
- `roc_auc`
- `precision`
- `recall`

---

# Example

**library(tidymodels)**  
*Loads the entire tidymodels ecosystem (rsample, recipes, parsnip, workflows, yardstick, etc.)*

**set.seed(123)**  
*Ensures reproducibility so the same random split is generated every time*

**split <- initial_split(mtcars, prop = 0.8)**  
*Splits data into 80% training and 20% testing data*
*Keeps structure of data reasonably consistent between splits*

**train_data <- training(split)**  
*Extracts the training dataset used to build the model*

**test_data  <- testing(split)**  
*Extracts the test dataset used only for final evaluation*

**rec <- recipe(mpg ~ ., data = train_data) %>%**  
*Defines a preprocessing pipeline*
*mpg is the target variable, all other variables are predictors*
*Uses only training data to avoid data leakage*

**step_corr(all_numeric(), threshold = 0.8)** %>%
Dont use correlated variables (average and median temp both) as predictors (double effect)

**step_normalize(all_numeric_predictors())**  
*Standardizes all numeric predictor variables*
*Transforms features to mean = 0 and standard deviation = 1*
*Helps models that are sensitive to scale*

[[Models, engines, and modes]]

**model <- linear_reg() %>%**  
*Specifies a linear regression model (not yet trained)*

**set_engine("lm")**  
**set_mode(“classification")**
*Uses base R linear model engine*
*Alternative engines include glmnet or stan*

**wf <- workflow() %>%**  
*Creates a unified modeling pipeline*

**add_recipe(rec) %>%**  
*Adds preprocessing steps to the workflow*

**add_model(model)**  
*Adds the model specification to the workflow*

**fit_model <- fit(wf, data = train_data)**  
*Trains the full workflow on training data*
*Applies preprocessing then fits the model*

**preds <- predict(fit_model, test_data) %>%**  
*Generates predictions on unseen test data*
*Output column is .pred (predicted values)*

**bind_cols(test_data)**  
*Combines predictions with actual test data for comparison*

**metrics <- metrics(preds, truth = mpg, estimate = .pred)**  
*Computes model performance metrics*
*Compares actual values (mpg) with predictions (.pred)*

**metrics**  
*Displays evaluation results such as RMSE and R²*