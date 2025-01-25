# Linear Regression Metrics and Methods

## Mean Absolute Error (MAE)
MAE measures the average absolute difference between predicted and actual values. It is given by:

```plaintext
MAE = (1/n) Σ |yᵢ - ŷᵢ|
```

- **Use Case:** MAE is used when you want to measure the average magnitude of errors without considering their direction (positive or negative).
- **When Not to Use:** MAE might not be ideal when large errors need to be penalized more than small ones.
- **In Loss Functions:** Suitable for robust models against outliers as it treats all errors equally.

## Mean Squared Error (MSE)
MSE measures the average of the squared differences between predicted and actual values:

```plaintext
MSE = (1/n) Σ (yᵢ - ŷᵢ)²
```

- **Use Case:** MSE is used when large errors need to be penalized more than small ones, as squaring emphasizes larger deviations.
- **When Not to Use:** MSE is sensitive to outliers, which can overly influence the loss.
- **In Loss Functions:** Commonly used for its smooth gradient, aiding optimization in gradient descent.

## Root Mean Squared Error (RMSE)
RMSE is the square root of MSE, providing the error in the same units as the target variable:

```plaintext
RMSE = √((1/n) Σ (yᵢ - ŷᵢ)²)
```

- **Use Case:** Interpreting the error in the same scale as the target variable.
- **When Not to Use:** Like MSE, it is sensitive to outliers.
- **In Loss Functions:** RMSE is typically avoided in loss functions due to its non-differentiable nature near zero.

## R-squared (R²)
R² measures the proportion of variance in the target variable explained by the model:

```plaintext
R² = 1 - (SSE/SST)
```

- **Use Case:** Evaluating how well the model explains variability in the target variable.
- **When Not to Use:** R² can be misleading in non-linear models or when adding irrelevant predictors artificially inflates the score.

## Variance Explained
Variance explained refers to the proportion of the total variability in the target variable that a model accounts for. It relates to R² but is broader in its interpretability.

> **Key Concepts:**
> - **Total Variance:** Variability of the target variable around its mean.
> - **Explained Variance:** Variability explained by the model.
> - **Residual Variance:** Variability left unexplained by the model.

## Ridge Regression
Ridge regression adds an L2 regularization term to the linear regression loss:

```plaintext
Loss = SSE + λ Σ βⱼ²
```

- **Why Called Ridge:** The term smooths coefficients, forming a "ridge" in parameter space.
- **How It Works:** Penalizes large coefficients, shrinking them but not setting them to zero.
- **Use Cases:** Multicollinearity, when all predictors are relevant.

## Lasso Regression
Lasso regression adds an L1 regularization term to the linear regression loss:

```plaintext
Loss = SSE + λ Σ |βⱼ|
```

- **Why Called Lasso:** Performs shrinkage and selection by forcing some coefficients to exactly zero.
- **How It Works:** Encourages sparsity by zeroing out irrelevant predictors.
- **Use Cases:** High-dimensional datasets requiring feature selection.

## Comparison: Ridge vs. Lasso

| **Aspect**           | **Ridge Regression**                  | **Lasso Regression**                  |
|-----------------------|----------------------------------------|----------------------------------------|
| **Penalty Term**      | L2-norm (Σ βⱼ²)                       | L1-norm (Σ |βⱼ|)                      |
| **Effect on Coefficients** | Shrinks coefficients but doesn’t set them to zero. | Shrinks coefficients and sets some to zero. |
| **Feature Selection** | No feature selection.                 | Performs feature selection.            |
| **Use Cases**         | Multicollinearity; retaining all features. | High-dimensional data; removing irrelevant features. |

## Elastic Net
Elastic Net combines Ridge and Lasso penalties:

```plaintext
Loss = SSE + λ₁ Σ |βⱼ| + λ₂ Σ βⱼ²
```

Useful for situations where multicollinearity exists and feature selection is needed.
