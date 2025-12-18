_Overview: Results & derivations for OLS results._

## Section 1: Ordinary Least Squares

### Simple Linear Regression

The simplest case for linear regression is with one covariate. Let us first consider the case where there is also no intercept term, so $\hat\beta$ is one-dimensional.

<div class="callout proposition"><span class="label">Proposition: Regression through the Origin with One Predictor</span><br/>
<hr style="height:0.01px; visibility:hidden;" />
Consider an independent and identically distributed sample $\{(X_i, Y_i) \}_{i=1}^{n}$ from the distribution $(X, Y) \in \mathscr P(\mathbb R)$.

Then the <i>least squares solution</i> $\hat\beta$ that goes through the origin $(0, 0)$ to estimate $\mathbb E[Y | X = x]$ is
$$\hat\beta = \left(\frac{1}{n} \sum_{i = 1}^n X_i^2\right)^{-1} \left(\frac{1}{n} \sum_{i = 1}^n X_i \cdot Y_i\right).$$

<details class="collapsible">
<summary>Derivation</summary>
<div class="collapsible__content">
Let $\{(Y_i, X_i) \}_{i=1}^{n}$ be a random sample from the distribution of $(Y, X)$. The function $S(b) = \mathop{\mathbb{E}}[(Y-X'b)^2]$ is unknown to us, but we can estimate it consistently with the following expression:

$$\hat{S}(b) = \frac{1}{n}\sum_{i=1}^{n} (Y_i - X_i'b)^2 = \frac{1}{n}\text{SSE}(b),$$

where SSE$(b) = \sum_{i=1}^{n}(Y_i - X_i'b)^2$ is the sum of the squared errors. Instead of minimizing $S(b)$, we can minimize $\hat{S}(b)$. This is the process that will yield the least squares estimator. More precisely, we have:

\begin{gather*}
    \hat{\beta} = \arg\min\_{b \in \mathbb{R}^K}\hat{S}(b) = \arg\min\_{b \in \mathbb{R}^K} \frac{1}{n} \sum_{i=1}^{n} (Y_i - X_i'b)^2
\end{gather*}
Let us proceed with the minimization.
\begin{gather*}
    \hat{S}(b) = \left(\frac{1}{n} \sum_{i=1}^{n} Y_i^2\right) - 2b'\left(\frac{1}{n} \sum_{i=1}^{n}X_iY_i \right) + b'\left(\frac{1}{n} \sum_{i=1}^{n} X_i X_i' \right)b 
    \\\\
    \frac{\delta}{\delta b} \hat{S}(b) = -2\left(\frac{1}{n}\sum_{i=1}^{n} X_iY_i \right) + 2 \left(\frac{1}{n} \sum_{i=1}^{n} X_iX_i'\right)b
\end{gather*}
Setting the above expression to zero, we get:
\begin{gather*}
    \frac{1}{n}\sum_{i=1}^{n} X_iY_i = \left( \frac{1}{n} \sum_{i=1}^{n} X_iX_i'\right)\hat{\beta} 
    \\\\
    \implies \hat{\beta} = \left( \frac{1}{n} \sum_{i=1}^{n} X_iX_i \right)^{-1} \left( \frac{1}{n} \sum_{i=1}^{n} X_iY_i \right),
\end{gather*}
</div>
</details>
</div>



<div class="callout definition"><span class="label">Definition: Object to Define</span><br/>
<hr style="height:0.01px; visibility:hidden;" />
Here is the definition. Here are the list of required properties:
<ol type="i">
  <li>property 1.</li>
  <li>property 2.</li>
  <li>property 3.</li>
</ol>
</div>

We now introduce a proposition.

<div class="callout proposition"><span class="label">Proposition: Property to Define</span><br/>
<hr style="height:0.01px; visibility:hidden;" />
Here is the proposition. <i>This only holds under the described circumstances</i>. <strong><i>We truly want to emphasize this.</i></strong>
</div>

<details class="collapsible">
  <summary>Proof</summary>
  <div class="collapsible__content">
  Here is the proof of the above proposition.
  <details class="collapsible">
      <summary>Proof of the sub-proposition.</summary>
      <div class="collapsible__content">
        Here is the sub-proof.
      </div>
    </details>
  </div>
</details>