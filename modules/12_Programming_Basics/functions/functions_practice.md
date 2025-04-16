
# R Functions – Part 2

## 🔍 Concepts Covered
- Why write functions
- Anatomy of a function in R
- Local vs. global scope
- Control flow
- Vectorization
- `...` (ellipsis)
- Nesting

---

## 1: Function Fundamentals

**1. `microscope_magnification()`**

Write a function called microscope_magnification() that calculates total magnification based on the objective and ocular lens magnification. Default ocular is 10x.

magnification = objective * ocular

### ✅ Solution

---

## 2: Conditional Logic

**2. `check_cell_viability()`**
Write a function called check_cell_viability() that takes a percentage (0–100) and returns:
- >85 → "Viable"
- 60–85 → "Borderline"
- <60 → "Non-viable"
- Invalid or `NA` → "Invalid"

### ✅ Solution

---

## 3: Loop + Scope

**3. `adjust_pipette()`**

Write a function called adjust_pipette() that takes a vector of volumes (in µL) and returns a new vector where:

Volumes less than 1 are set to 1

Volumes greater than 1000 are set to 1000

Other volumes stay the same

Complete the function below. 

### ✅ Solution

```r

adjust_pipette <- function(volumes) {
  adjusted <- numeric(length(volumes)) #what is the purpose of this line?
  
  # in the line below, get indices for looping over volumes vector, you can use seq_along(volumes)
  for () { 

  }
  
  return(adjusted)
}

```
---

## 4: Vectorized + Nested Functions

**4. `scale_and_round()`**

Create a function called scale_and_round() that:

Takes a numeric vector

Multiplies every element by 1000

Rounds to the nearest whole number a.k.a nest in `log10()`.

### ✅ Solution

---

## 5: Using `...`

**5. `quick_stats()`**

Write a function called quick_stats() that:

Takes a numeric vector x

Uses ... to pass additional arguments to mean() and sd()

Returns a named list with mean and standard deviation
hint: Use `...` to pass `na.rm = TRUE` into mean and sd.

### ✅ Solution

---

## 6. Cumulative Exercise

Write a function cell_cycle_summary() that takes a numeric vector of cell cycle phase durations (in hours). The function should:

Replace any negative values with NA

Print a warning for any durations > 24 (likely erroneous)

Return a named list that includes:

Total duration (rounded)

Average phase length (rounded)

Number of missing values

Use a for loop for cleaning, and vectorized + nested functions for summary.

### ✅ Solution

---

## 7. Calculate mean by group 
Write a function mean_by_group() that takes two vectors:

values: a numeric vector

groups: a character or factor vector (same length)

Return a named vector with the mean of values for each group

### ✅ Solution

---

## 8. Plot Cell Counts by Condition
Write a function called plot_cell_counts() that:

Takes a data frame with two columns:

condition: a character or factor column with experimental conditions (e.g., "Control", "Treatment")

count: a numeric column representing the number of cells observed

Returns a bar plot of average cell count per condition using ggplot2.

### ✅ Solution

```r
# Example data:
df <- data.frame(
  condition = c("Control", "Control", "Treatment", "Treatment"),
  count = c(100, 120, 200, 220)
)

# Use the function
plot_cell_counts(df)
```
---