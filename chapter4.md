## 第四章

### I 证明下述结论

1° 若 \( A = A^T \in \mathbf{R}_r^{n \times n} \)，则存在 \( A_i = A_i^T \in \mathbf{R}\_1^{n \times n} \) 使  
\[
A = \sum_{i=1}^r A_i.
\]

2° 若 \( A = A^T \in \mathbf{R}^{n \times n} \)，且满足  
\[
x^T A x = 0, \quad x \in \mathbf{R}^n,
\]
则 \( A = 0 \).

3° 一个实二次型可以分解成两个实系数的一次齐次式之积，当且仅当下述两者之一成立：

- (a) 二次型对应矩阵秩为 1.
- (b) 二次型对应矩阵秩为 2 且正负惯性指数相同.

4° 对任何 \( A = A^H \in \mathbf{C}^{n \times n} \)，总存在 \( t > 0 \)，使得 \( A + tI_n \) 是正定矩阵.

5° \( A \) 正定当且仅当 \( A^{-1} \) 正定.

6° 若 \( A = A^T \in \mathbf{R}^{n \times n} \)，且 \( \det(A) < 0 \)，则存在 \( x \in \mathbf{R}^n \)，使得 \( x^T A x < 0 \).

7° 若 \( A = A^H \in \mathbf{C}^{n \times n} \) 正定，则存在 \( \alpha, \beta \in \mathbf{R} \) 均正，使得  
\[
\alpha x^H x \leqslant x^H A x \leqslant \beta x^H x, \quad x \in \mathbf{C}^n.
\]

8° 若 \( a = [1, 1, \cdots, 1]^T \)，则 \( nx^T x - (a^T x)^2 \) 是 \( x \in \mathbf{R}^n \) 的半正定二次型.

9° 若 \( A = A^T \in \mathbf{R}^{n \times n} \)，且存在 \( x_1, x_2 \in \mathbf{R}^n \)，使得  
\[
x_1^T A x_1 > 0, \quad x_2^T A x_2 < 0,
\]
则存在\(0 \neq x_0 \in \mathbf{R}^{n}\)使\(x_0^{T}Ax_0=0\).

#### 证明 1°

由惯性定理知
对于 \(\forall A = A^T \in \mathbf{R}_r^{n \times n} \)，有可逆矩阵 Q，使得：
\[
A = Q^T \begin{pmatrix}
I_p & & \\
& -I_q & \\
& & 0
\end{pmatrix} Q
\]
由此有：
\[
A = \sum_{i=1}^{p} Q^T B_i Q - \sum_{j=p+1}^{p+q} Q^T B_j Q
\]
其中，\( B_i = \begin{pmatrix} 0 & \cdots & 0 & \cdots & 0 \\ \vdots & & \vdots & & \vdots \\ 0 & \cdots & 1 & \cdots & 0 \\ \vdots & & \vdots & & \vdots \\ 0 & \cdots & 0 & \cdots & 0 \end{pmatrix}, \) 第\(i\)行为 1
令
\[
A_{i} =
\begin{cases}
Q^T B_i Q, & 1 \leq i \leq p \\
-Q^T B_i Q, & p+1 \leq i \leq r
\end{cases}
\]\(
\mathrm{rank}(A_i) = 1
\)
证毕。

#### 证明 2°

法 1.常规做法
由惯性定理知
对于 \(\forall A = A^T \in \mathbf{R}_r^{n \times n} \)，有可逆矩阵 Q，使得：
\[
A = Q^T \begin{pmatrix}
I_p & & \\
& -I_{r-p} & \\
& & 0
\end{pmatrix} Q
\]
由此有：\(\forall x \in \mathbf{R}^n \)，\( x^T A x = 0 \)，令 \( y = Q^{-1} x \)，则有：\(y^T A y = 0\)
此时：
\[
y^T A y = x^T
\begin{pmatrix}
I_p & & \\
& -I_{r-p} & \\
& & 0
\end{pmatrix}
x = 0, \quad \forall x \in \mathbf{R}^n
\]
令\(x = e_1, \) 则 \(p=0\).
令\(x = e_{p+1}, \) 则 \(r-p=0\)，得\(r=0\)，证毕.

\(A^T \neq A\)时，反例如：\(A=\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix},
x^TAx=
\begin{pmatrix}
\xi_1 & \xi_2 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
\xi_1\\
\xi_2
\end{pmatrix}\equiv0,\forall x \in \mathbf{R}^3
\)，但\(A\neq 0.\)即反对称矩阵为所有反例.

法 2.导数做法
若 \( x^T A x = 0 \)，则\(
\dfrac{\partial (x^T A x)}{\partial x^T} = (A^T + A)x = 0, \,\forall x
\)
因此\(A^T + A = 0\)，且\(A^T = A\)，则\( A = 0 \).

#### 证明 3°





#### 证明 4°
\( A + tI_n \) 的特征值为 \( \lambda(A + tI_n) = \lambda(A) + t \)，其中 \( \lambda(A) \) 为矩阵 \( A \) 的特征值。
令 \( \lambda_{\min} = \min \lambda(A) \)，当 \( t > |\lambda\_{\min}| \) 时，矩阵 \( A + tI_n \) 的所有特征值均为正。
又因为 \( A + tI_n \) 是 Hermit 矩阵，因此它是正定矩阵。

注：Hermit 矩阵的特征值为实数.

#### 证明 5°




#### 证明 6°
设 \( A = A^T \in \mathbf{R}^{n \times n} \)，则 \( A \) 的特征值 \( \lambda_1, \ldots, \lambda_n \) 均为实数。
由于 \( \det(A) = \prod_{i=1}^n \lambda_i < 0 \)，可知至少存在 \( \lambda_k < 0 \)。
令 \( x \) 满足 \( Ax = \lambda_k x \) ，且 \( x \neq 0 \)。
则有：
   \[
   x^T A x = x^T x \cdot \lambda_k < 0
   \]
   其中 \( x^T x > 0 \)。
证毕。

#### 证明 7°
\( A \) 是正定矩阵，因此 \( A \) 是正规矩阵。
存在酉矩阵 \( U \)，使得 \( A = U^{H} \operatorname{diag}(\lambda_1, \ldots, \lambda_n) U \)，其中 \( \lambda_i > 0 \)。
因此，对于任意 \( x \)，有：
   \[
   x^{H} A x = (Ux)^{H} \operatorname{diag}(\lambda_1, \ldots, \lambda_n) (Ux)
   \]

推导出：
   \[
   (\min \lambda_i) (Ux)^{H} (Ux) \leq x^{H} A x \leq (\max \lambda_i) (Ux)^{H} (Ux), \quad 1 \leq i \leq n
   \]

即：
   \[
   (\min \lambda_i) x^{H} x \leq x^{H} A x \leq (\max \lambda_i) x^{H} x, \quad 1 \leq i \leq n
   \]

#### 证明 8°
给定的二次型可以化简为矩阵形式：
\[
n x^T x - (a^T x)^2 = n x^T x - (x^T a)(a^T x) = x^T (nI_n - aa^T) x
\]
因此，问题转化为证明矩阵 \( nI_n - aa^T \) 是半正定的。
\( a \) 是全为 \( 1 \) 的列向量，即 \( a = [1, 1, \cdots, 1]^T \)。  
矩阵 \( aa^T \) 是一个 秩为 1 的对称矩阵，它的特征值分布为：
- 一个非零特征值：  
     \[
     \lambda = a^T a = [1, 1, \cdots, 1]^T [1, 1, \cdots, 1] = n
     \]

- 剩下的 \( n-1 \) 个特征值为 \( 0 \)。


矩阵 \( nI_n - aa^T \) 的特征值
利用矩阵的性质：若 \( M = nI_n - aa^T \)，则 \( M \) 的特征值为 \( n - \lambda \)，其中 \( \lambda \) 是 \( aa^T \) 的特征值。  
因此：
- 当 \( \lambda = n \) 时，矩阵 \( M \) 的特征值为 \( n - n = 0 \)；
- 当 \( \lambda = 0 \) 时，矩阵 \( M \) 的特征值为 \( n - 0 = n \)。

所以，矩阵 \( nI_n - aa^T \) 的所有特征值为非负值（\( n \) 或 \( 0 \)）。
由于矩阵 \( nI_n - aa^T \) 的特征值均为非负，因此它是半正定的。  


#### 证明 9°
法 1.惯性定理
根据惯性定理，矩阵 \( M^T A M = \operatorname{diag}(I_p, -I_{r-p},  0)\)，其中 \( p \geq 1 \)，\( r-p \geq 1 \)。
构造向量 \( x_p = ((1, 0, \ldots, 0, 1, 0, \ldots, 0) M^{-T})^T \)，从而得证。

法 2.介值定理（函数连续，两点异号）
构造 \( \varphi(t) = x^T(t) A x(t) \)，其中 \( x(t) =  t x_2 + (1-t) x_1 \)。
初始条件：\( \varphi(0) = x_1^T A x_1 > 0 \)， \( \varphi(1) = x_2^T A x_2 < 0 \)。
根据连续性，存在 \( t_0 \in (0, 1) \)，使得 \( \varphi(t_0) = 0 \)，即 \( x(t_0)^T A x(t_0) = 0 \)。
令 \( x_0 = x(t_0)\),下面证明 \( x(t_0) \neq 0 \)。

假设 \( x(t_0) = 0 \)，其中 \( t_0 \in (0, 1) \)。
由 \( x(t_0) = t_0 x_2 + (1 - t_0) x_1 = 0 \) 得：
   \[
   x_2 = -\frac{1 - t_0}{t_0} x_1 \triangleq \alpha_0 x_1
   \]
进而有：
   \[
   x_2^T A x_2 = \alpha_0^2 x_1^T A x_1 > 0
   \]
与题设条件矛盾。证毕


#### 证明 1°

### III 证明以下各题

#### 证明 6°

定义 \( H_n = (a_{ij})_{n \times n} \)，
其中 \( a_{ij} = \dfrac{1}{i + j - 1} \)。

\[ x^T H_n x = \sum_{i=1}^{n} \sum_{j=1}^{n} a_{ij} \xi_i \xi_j \\= \sum_{i,j=1}^{n} \dfrac{1}{i + j - 1} \xi_i \xi_j\\=
\]

化简得：
\[
x^T H_n x = \sum_{i,j=1}^{n} \int_{0}^{1} t^{i + j - 2} dt, \quad i \leq j
\]

进一步化为：
\[
x^T H_n x = \int_{0}^{1} \sum_{i,j=1}^{n} (t^{j-1} \xi_i t^{j-1} \xi_j) dt
\]
化为平方形式：
\[
x^T H_n x = \int_{0}^{1} \left(\sum_{i=1}^{n} t^{i-1} \xi_i\right)^2 dt > 0,\quad x \neq 0
\]
证毕。
