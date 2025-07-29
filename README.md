### 🔶 Handling Missing Values in NumPy

This section covers how to detect and handle missing data (`np.nan`) in NumPy arrays using built-in functions and column-wise logic.

📌 **Key Concepts:**
- 🔍 Detect NaNs: `np.isnan()`
- ➕ Replace NaNs with:
  - Fixed values (`0`, `-1`, etc.)
  - Mean or median of the column (`np.nanmean()`, `np.nanmedian()`)
- 🧹 Remove NaNs using boolean masking
- 🔁 Column-wise NaN replacement using loops

📂 **Examples Covered:**
- Replace all NaNs in a 1D/2D array with a constant
- Replace NaNs with column mean:
  ```python
  for i in range(arr.shape[1]):
      arr[np.isnan(arr[:, i]), i] = mean_val[i]
  ```
- Replace NaNs with column median
- Count NaNs in each row or column: `np.isnan(arr).sum(axis=1)`

🧪 Helpful for real-world data cleaning and preparation in NumPy-based pipelines.
