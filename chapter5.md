## 第五章

### I 证明下述结论
1° 在 \( \mathbf{R}^1 \) 中，任何范数 \( \nu(x) \) 都必定具有形式：  
\[
\nu(x) = \lambda |x|, \quad \lambda > 0
\]


4° 若 \( \alpha_i > 0, \; i \in \underline{n} \)，则\(
\left[\sum_{i=1}^n \alpha_i |\xi_i|^2\right]^{\frac{1}{2}}\)是 \( x \in \mathbf{C}^n \) 的范数。

#### 证明 1°

1.验证正定性
\(\nu(x) > 0\) 当且仅当 \(x \neq 0\)。因此，\(\lambda > 0\)。
2.验证齐次性
令 \(x \in \mathbf{R}\)，对于任意标量 \(\alpha \in \mathbf{R}\)，齐次性条件要求：\(\nu(\alpha x) = |\alpha| \nu(x).\)
3.验证三角不等式
对于任意 \( x, y \in \mathbf{R} \):\(\mathrm{v(x+y) \leq v(x) + v(y)}\)
代入已知形式：\( \lambda |x+y| \leq \lambda |x| + \lambda |y| \)
由于 \( \lambda > 0 \)，等价于：\( |x+y| \leq |x| + |y| \)

#### 证明 4°
1.正定性
因为 \( \alpha_i > 0 \) 且 \( |\xi_i|^2 \geq 0 \)，所以 \( \sum \alpha_i |\xi_i|^2 \geq 0 \)。
因此 \( \|x\| = \left[\sum \alpha_i |\xi_i|^2\right]^{1/2} \geq 0 \)。
\( \|x\| = 0 \) 当且仅当 \( x = 0 \)
若 \( \|x\| = 0 \)，则 \( \sum \alpha_i |\xi_i|^2 = 0 \)。
由于 \( \alpha_i > 0 \)，所以每一项 \( |\xi_i|^2 = 0 \)。
因此 \( \xi_i = 0 \)（\( i = 1, \dots, n \)），即 \( x = 0 \)。
反之显然成立。

2.齐次性
对任意复数 \( k \)，需证 \( \|kx\| = |k| \|x\| \)。
\(\|kx\| = \left[\sum \alpha_i |k\xi_i|^2\right]^{1/2} = \left[\sum \alpha_i |k|^2 |\xi_i|^2\right]^{1/2} = |k| \left[\sum \alpha_i |\xi_i|^2\right]^{1/2} = |k| \|x\|\)

3.三角不等式
需证 \( \|x + y\| \leq \|x\| + \|y\| \)。
使用 Cauchy-Schwarz 不等式：

\[
\|x + y\|^2 = \sum \alpha_i |(\xi_i + \eta_i)|^2 = \sum \alpha_i \left(|\xi_i|^2 + \xi_i \overline{\eta_i} + \overline{\xi_i} \eta_i + |\eta_i|^2\right)
\]

\[
\|x + y\|^2 = \|x\|^2 + \|y\|^2 + 2\operatorname{Re}\left(\sum \alpha_i \xi_i \overline{\eta_i}\right)
\]

由 Cauchy-Schwarz 不等式：

\[
\left|\sum \alpha_i \xi_i \overline{\eta_i}\right| \leq \left[\sum \alpha_i |\xi_i|^2\right]^{1/2} \left[\sum \alpha_i |\eta_i|^2\right]^{1/2} = \|x\| \|y\|
\]

因此：\(\|x + y\|^2 \leq \|x\|^2 + \|y\|^2 + 2\|x\| \|y\| = (\|x\| + \|y\|)^2\)

所以：\(\|x + y\| \leq \|x\| + \|y\|\)

---

### IV 证明下述结论
1° \( ||AB||_F \leqslant \min \{ ||A||_2 ||B||_F, ||A||_F ||B||_2 \} \)

2° 若 \( A \in \mathbf{U}^{n \times l} \)，则 \( ||A||_2 = 1 \)，\( ||A||_F = \sqrt{l} \)


6° 若 \( \nu \) 为 \( \mathbf{C}^{n \times n} \) 的任一范数，则存在 \( \lambda > 0 \) 使得 \( \mu(A) = \lambda \nu(A) \) 为相容范数。


#### 证明 1°
分两部分证明：
1.\( \|AB\|_F \leq \|A\|_2\|B\|_F \)
2.\( \|AB\|_F \leq \|A\|_F\|B\|_2 \)

证明 (1)：\( \|AB\|_F \leq \|A\|_2\|B\|_F \)
由 Frobenius 范数定义：\(\|AB\|_F^2 = \operatorname{tr}((AB)^H (AB)) = \operatorname{tr}(B^H A^H AB)\)
由谱范数的定义，对任意向量 \( x \) 有：\(\|Ax\|_2 \leq \|A\|_2\|x\|_2\)，因此 \( A^H A \leq \|A\|_2^2I \)。
结合迹的单调性：\(\operatorname{tr}(B^H A^H AB) \leq \|A\|_2^2 \operatorname{tr}(B^H B)\)，即：\(\|AB\|_F^2 \leq \|A\|_2^2\|B\|_F^2\)
开平方得到：\(\|AB\|_F \leq \|A\|_2\|B\|_F\)

证明 (2)：\( \|AB\|_F \leq \|A\|_F\|B\|_2 \)
对矩阵 \( B \) 进行 SVD 分解：\(B = V_1\Sigma V_2^H\)其中 \( V_1 \) 和 \( V_2 \) 是酉矩阵，\( \Sigma \) 是对角矩阵。
由于对酉正矩阵，Frobenius 范数不变：\(\|AB\|_F = \|AV_1\Sigma V_2^H\|_F = \|AV_1\Sigma\|_F\)
设 \( AV_1 \) 的第 \( i \) 列为 \( x_i \)，\( \Sigma \) 的第 \( i \) 个对角元为 \( \sigma_i \)，则：\(
\|AB\|_F^2 = \sum_i \|x_i\sigma_i\|_2^2 = \sum_i \|x_i\_2^2\sigma_i^2\)
根据最大值性质：\(\|AB\|_F^2 \leq (\max_i \sigma_i^2) \sum_i \|x_i\|_2^2\)因为 \( \|B\|_2^2 = \max_i \sigma_i^2 \)，所以：\(\|AB\|_F^2 \leq \|B\|_2^2\|A\|_F^2\)
开平方得到：\(\|AB\|_F \leq \|A\|_F\|B\|_2\)


#### 证明 2°
酉矩阵的性质
1.\( A^H A = A A^H = I \)（单位矩阵）。
2.每一列（行）都是单位向量。
3.不同列（行）之间正交。

证明 \( \|A\|_2 = 1 \)
范数定义：  \(\|A\|_2 = \sqrt{\lambda_{\max}(A^H A)}\)
其中 \( \lambda_{\max} \) 表示矩阵 \( A^H A \) 的最大特征值。
由于 \( A \) 是酉矩阵，满足 \( A^H A = I \)。
单位矩阵 \( I \) 的所有特征值都是 1。
因此：\(\|A\|_2 = \sqrt{1} = 1\)

证明 \( \|A\|_F = \sqrt{l} \)
范数定义：\(\|A\|_F = \sqrt{\sum_{i,j} |a_{ij}|^2}\)其中 \( a_{ij} \) 是矩阵 \( A \) 的元素。
另一种表示形式：\(\|A\|_F = \sqrt{\operatorname{tr}(A^H A)}\)其中 \( \operatorname{tr} \) 表示矩阵的迹。
由于 \( A^H A = I \)，则 \( \operatorname{tr}(A^H A) = \operatorname{tr}(I) = l \)，其中 \( l \) 是矩阵 \( A \) 的列数。
因此：\(\|A\|_F = \sqrt{l}\)


#### 证明 6°
步骤 1：利用范数等价性
由于 \( \nu \) 是范数，存在正常数 \( c_1, c_2 \)，使得对任意矩阵 \( A \)，有：\(c_1\|A\|_\infty \leq \nu(A) \leq c_2\|A\|_\infty\)

步骤 2：利用无穷范数的相容性
对于任意矩阵 \( A, B \)，我们知道：\(\|AB\|_\infty \leq n\|A\|_\infty\|B\|_\infty\)，其中 \( n \) 是矩阵的维数。

步骤 3：建立不等式链
对于任意矩阵 \( A, B \)：\(\nu(AB) \leq c_2\|AB\|_\infty \leq c_2n\|A\|_\infty\|B\|_\infty\)由范数等价性：\(\|A\|_\infty \leq \dfrac{\nu(A)}{c_1}, \quad \|B\|_\infty \leq \dfrac{\nu(B)}{c_1}\)
因此：\(\nu(AB) \leq c_2n\left(\dfrac{\nu(A)}{c_1}\right)\left(\dfrac{\nu(B)}{c_1}\right) = \dfrac{c_2n}{c_1^2}\nu(A)\nu(B)
\)

步骤 4：定义 \( \lambda \)
令：\(\lambda = \sqrt{\dfrac{c_2n}{c_1^2}}\)
定义新的范数：\(\mu(A) = \lambda \nu(A)\)

步骤 5：验证相容性
对于任意矩阵 \( A, B \)：\(\mu(AB) = \lambda \nu(AB) \leq \lambda \dfrac{c_2n}{c_1^2}\nu(A)\nu(B) = \lambda^2 \nu(A)\nu(B)\)
由于 \( \mu(A) = \lambda \nu(A) \)，所以：\(\mu(AB) \leq \mu(A)\mu(B)\)，证明了 \( \mu(A) \) 是相容范数。
