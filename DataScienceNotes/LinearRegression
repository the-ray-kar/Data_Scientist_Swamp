<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Linear Regression Metrics and Methods</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 20px;
            background-color: #f9f9f9;
        }
        h1, h2, h3 {
            color: #333;
        }
        h1 {
            border-bottom: 2px solid #333;
            padding-bottom: 10px;
        }
        ul {
            margin: 10px 0;
            padding-left: 20px;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
            font-size: 0.95em;
        }
        .note {
            background-color: #e7f3fe;
            border-left: 4px solid #2196F3;
            padding: 10px;
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <h1>Linear Regression Metrics and Methods</h1>

    <h2>Mean Absolute Error (MAE)</h2>
    <p>MAE measures the average absolute difference between predicted and actual values. It is given by:</p>
    <pre><code>MAE = (1/n) Σ |yᵢ - ŷᵢ|</code></pre>
    <ul>
        <li><strong>Use Case:</strong> MAE is used when you want to measure the average magnitude of errors without considering their direction (positive or negative).</li>
        <li><strong>When Not to Use:</strong> MAE might not be ideal when large errors need to be penalized more than small ones.</li>
        <li><strong>In Loss Functions:</strong> Suitable for robust models against outliers as it treats all errors equally.</li>
    </ul>

    <h2>Mean Squared Error (MSE)</h2>
    <p>MSE measures the average of the squared differences between predicted and actual values:</p>
    <pre><code>MSE = (1/n) Σ (yᵢ - ŷᵢ)²</code></pre>
    <ul>
        <li><strong>Use Case:</strong> MSE is used when large errors need to be penalized more than small ones, as squaring emphasizes larger deviations.</li>
        <li><strong>When Not to Use:</strong> MSE is sensitive to outliers, which can overly influence the loss.</li>
        <li><strong>In Loss Functions:</strong> Commonly used for its smooth gradient, aiding optimization in gradient descent.</li>
    </ul>

    <h2>Root Mean Squared Error (RMSE)</h2>
    <p>RMSE is the square root of MSE, providing the error in the same units as the target variable:</p>
    <pre><code>RMSE = √((1/n) Σ (yᵢ - ŷᵢ)²)</code></pre>
    <ul>
        <li><strong>Use Case:</strong> Interpreting the error in the same scale as the target variable.</li>
        <li><strong>When Not to Use:</strong> Like MSE, it is sensitive to outliers.</li>
        <li><strong>In Loss Functions:</strong> RMSE is typically avoided in loss functions due to its non-differentiable nature near zero.</li>
    </ul>

    <h2>R-squared (R²)</h2>
    <p>R² measures the proportion of variance in the target variable explained by the model:</p>
    <pre><code>R² = 1 - (SSE/SST)</code></pre>
    <ul>
        <li><strong>Use Case:</strong> Evaluating how well the model explains variability in the target variable.</li>
        <li><strong>When Not to Use:</strong> R² can be misleading in non-linear models or when adding irrelevant predictors artificially inflates the score.</li>
    </ul>

    <h2>Variance Explained</h2>
    <p>Variance explained refers to the proportion of the total variability in the target variable that a model accounts for. It relates to R² but is broader in its interpretability.</p>

    <div class="note">
        <strong>Key Concepts:</strong>
        <ul>
            <li>Total Variance: Variability of the target variable around its mean.</li>
            <li>Explained Variance: Variability explained by the model.</li>
            <li>Residual Variance: Variability left unexplained by the model.</li>
        </ul>
    </div>

    <h2>Ridge Regression</h2>
    <p>Ridge regression adds an L2 regularization term to the linear regression loss:</p>
    <pre><code>Loss = SSE + λ Σ βⱼ²</code></pre>
    <ul>
        <li><strong>Why Called Ridge:</strong> The term smooths coefficients, forming a “ridge” in parameter space.</li>
        <li><strong>How It Works:</strong> Penalizes large coefficients, shrinking them but not setting them to zero.</li>
        <li><strong>Use Cases:</strong> Multicollinearity, when all predictors are relevant.</li>
    </ul>

    <h2>Lasso Regression</h2>
    <p>Lasso regression adds an L1 regularization term to the linear regression loss:</p>
    <pre><code>Loss = SSE + λ Σ |βⱼ|</code></pre>
    <ul>
        <li><strong>Why Called Lasso:</strong> Performs shrinkage and selection by forcing some coefficients to exactly zero.</li>
        <li><strong>How It Works:</strong> Encourages sparsity by zeroing out irrelevant predictors.</li>
        <li><strong>Use Cases:</strong> High-dimensional datasets requiring feature selection.</li>
    </ul>

    <h2>Comparison: Ridge vs. Lasso</h2>
    <table border="1" cellspacing="0" cellpadding="5">
        <tr>
            <th>Aspect</th>
            <th>Ridge Regression</th>
            <th>Lasso Regression</th>
        </tr>
        <tr>
            <td>Penalty Term</td>
            <td>L2-norm (Σ βⱼ²)</td>
            <td>L1-norm (Σ |βⱼ|)</td>
        </tr>
        <tr>
            <td>Effect on Coefficients</td>
            <td>Shrinks coefficients but doesn’t set them to zero.</td>
            <td>Shrinks coefficients and sets some to zero.</td>
        </tr>
        <tr>
            <td>Feature Selection</td>
            <td>No feature selection.</td>
            <td>Performs feature selection.</td>
        </tr>
        <tr>
            <td>Use Cases</td>
            <td>Multicollinearity; retaining all features.</td>
            <td>High-dimensional data; removing irrelevant features.</td>
        </tr>
    </table>

    <h2>Elastic Net</h2>
    <p>Elastic Net combines Ridge and Lasso penalties:</p>
    <pre><code>Loss = SSE + λ₁ Σ |βⱼ| + λ₂ Σ βⱼ²</code></pre>
    <p>Useful for situations where multicollinearity exists and feature selection is needed.</p>
</body>
</html>
