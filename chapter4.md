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
对于 \(\forall A = A^T \in \mathbf{R}_r^{n \times n} \)，有可逆矩阵 Q，使得：\(
A = Q^T \begin{pmatrix}
I_p & & \\
& -I_q & \\
& & 0
\end{pmatrix} Q
\)
由此有：\(
A = \sum_{i=1}^{p} Q^T B_i Q - \sum_{j=p+1}^{p+q} Q^T B_j Q
\)
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

A正定，A的所有特征值均为正，\(A^{-1}\)特征值也为正

#### 证明 6°
设 \( A = A^T \in \mathbf{R}^{n \times n} \)，则 \( A \) 的特征值 \( \lambda_1, \ldots, \lambda_n \) 均为实数。
由于 \( \det(A) = \prod_{i=1}^n \lambda_i < 0 \)，可知至少存在 \( \lambda_k < 0 \)。
令 \( x \) 满足 \( Ax = \lambda_k x \) ，且 \( x \neq 0 \)。
则有：\(x^T A x = x^T x \cdot \lambda_k < 0\)，其中 \( x^T x > 0 \)。证毕。

#### 证明 7°
\( A \) 是正定矩阵，因此 \( A \) 是正规矩阵。
存在酉矩阵 \( U \)，使得 \( A = U^{H} \operatorname{diag}(\lambda_1, \ldots, \lambda_n) U \)，其中 \( \lambda_i > 0 \)。
因此，对于任意 \( x \)，有：\(x^{H} A x = (Ux)^{H} \operatorname{diag}(\lambda_1, \ldots, \lambda_n) (Ux)\)
推导出：\((\min \lambda_i) (Ux)^{H} (Ux) \leq x^{H} A x \leq (\max \lambda_i) (Ux)^{H} (Ux), \quad 1 \leq i \leq n\)
即：\((\min \lambda_i) x^{H} x \leq x^{H} A x \leq (\max \lambda_i) x^{H} x, \quad 1 \leq i \leq n\)

#### 证明 8°
给定的二次型可以化简为矩阵形式：
\[
n x^T x - (a^T x)^2 = n x^T x - (x^T a)(a^T x) = x^T (nI_n - aa^T) x
\]
因此，问题转化为证明矩阵 \( nI_n - aa^T \) 是半正定的。
\( a \) 是全为 \( 1 \) 的列向量，即 \( a = [1, 1, \cdots, 1]^T \)。  
矩阵 \( aa^T \) 是一个 秩为 1 的对称矩阵，它的特征值分布为：
一个非零特征值：\(\lambda = a^T a = [1, 1, \cdots, 1]^T [1, 1, \cdots, 1] = n\)
剩下的 \( n-1 \) 个特征值为 \( 0 \)。

矩阵 \( nI_n - aa^T \) 的特征值
利用矩阵的性质：若 \( M = nI_n - aa^T \)，则 \( M \) 的特征值为 \( n - \lambda \)，其中 \( \lambda \) 是 \( aa^T \) 的特征值。  
因此：
- 当 \( \lambda = n \) 时，矩阵 \( M \) 的特征值为 \( n - n = 0 \)；
- 当 \( \lambda = 0 \) 时，矩阵 \( M \) 的特征值为 \( n - 0 = n \)。

所以，矩阵 \( nI_n - aa^T \) 的所有特征值为非负值（\( n \) 或 \( 0 \)）。
由于矩阵 \( nI_n - aa^T \) 的特征值均为非负，因此它是半正定的。  


#### 证明 9°
==法 1.惯性定理==
根据惯性定理，矩阵 \( M^T A M = \operatorname{diag}(I_p, -I_{r-p},  0)\)，其中 \( p \geq 1 \)，\( r-p \geq 1 \)。
构造向量 \( x_p = ((1, 0, \ldots, 0, 1, 0, \ldots, 0) M^{-T})^T \)，从而得证。

==法 2.介值定理（函数连续，两点异号）==
构造 \( \varphi(t) = x^T(t) A x(t) \)，其中 \( x(t) =  t x_2 + (1-t) x_1 \)。
初始条件：\( \varphi(0) = x_1^T A x_1 > 0 \)， \( \varphi(1) = x_2^T A x_2 < 0 \)。
根据连续性，存在 \( t_0 \in (0, 1) \)，使得 \( \varphi(t_0) = 0 \)，即 \( x(t_0)^T A x(t_0) = 0 \)。
令 \( x_0 = x(t_0)\),下面证明 \( x(t_0) \neq 0 \)。
假设 \( x(t_0) = 0 \)，其中 \( t_0 \in (0, 1) \)。
由 \( x(t_0) = t_0 x_2 + (1 - t_0) x_1 = 0 \) 得：\(x_2 = -\frac{1 - t_0}{t_0} x_1 \triangleq \alpha_0 x_1\)
进而有：\(x_2^T A x_2 = \alpha_0^2 x_1^T A x_1 > 0\)
与题设条件矛盾。证毕

---


### II 证明以下各题
1.若 \( a_i, b_j \in \mathbf{R}^n, \, i \in \underline{m}, \, j \in \underline{l} \)，则 \(A = \sum_{i=1}^m a_i a_i^T - \sum_{j=1}^l b_j b_j^T\)的正惯性指数 \(\leqslant m\)，而负惯性指数 \(\leqslant l\)。

2.若 \( A = A^T \in \mathbf{R}^{n \times n} \)，则 \( A \) 正定当且仅当存在 \( b_i \in \mathbf{R}^n, \, i \in \underline{n} \) 使得  \(A = \sum_{i=1}^n b_i b_i^T\)，且 \(\operatorname{rank}[b_1, b_2, \cdots, b_n] = n\)。

3.若 \( A = -A^T \in \mathbf{R}^{n \times n} \)，则 \(\operatorname{rank}(A)\) 为偶数。


5.若 \( A = A^T \in \mathbf{R}^{n \times n} \) 正定，则  \(f(x) = \det\begin{bmatrix}A & x \\ x^T & 0\end{bmatrix}\)是 \( x \in \mathbf{R}^n \) 的负定二次型。


#### 证明 1°
第一部分：理解问题
首先明确几个概念：
- 正惯性指数 是指实对称矩阵的正特征值的个数
- 负惯性指数 是指实对称矩阵的负特征值的个数
- 矩阵 \( A \) 是实对称矩阵，因为 \( a_i a_i^T \) 和 \( b_j b_j^T \) 都是实对称矩阵

第二部分：分析第一项 \( \sum_{i=1}^m a_i a_i^T \)
对于每个向量 \( a_i \)，\( a_i a_i^T \) 是一个秩为1的半正定矩阵
\( \sum_{i=1}^m a_i a_i^T \) 是 \( m \) 个半正定矩阵的和
根据秩的性质，\( \text{rank}(\sum_{i=1}^m a_i a_i^T) \leq m \)
因此，第一项至多有 \( m \) 个正特征值

第三部分：分析第二项 \( -\sum_{j=1}^l b_j b_j^T \)
\( \sum_{j=1}^l b_j b_j^T \) 是半正定矩阵
取负后，\( -\sum_{j=1}^l b_j b_j^T \) 是半负定矩阵
同理，\( \text{rank}(\sum_{j=1}^l b_j b_j^T) \leq l \)
因此，第二项至多贡献 \( l \) 个负特征值

#### 证明 2°
必要性（⇒）
假设 A 正定，证明存在满足条件的 \(b_i\)。
由于 A 正定，存在正交矩阵 P 和对角矩阵 Λ，使得：\( A = P\Lambda P^T \)，其中 \(Λ = diag(λ_1, λ_2, ..., λ_n)\)，且所有 \(λ_i > 0\).
令 \( B = P\sqrt{\Lambda} \)，其中 \(\sqrt{\Lambda} = \text{diag}(\sqrt{λ_1}, \sqrt{λ_2}, ..., \sqrt{λ_n})\)，则 \( A = BB^T \)
记 B 的列向量为 \(b_i\)，即 \( B = [b_1, b_2, ..., b_n] \)，则 \( A = \sum_{i=1}^n b_i b_i^T \).
因为 P 是正交矩阵，Λ 的对角元素都大于0，所以：\( \text{rank}[b_1, b_2, ..., b_n] = \text{rank}(B) = n \).

充分性（⇐）
假设存在 \(b_i\) 满足条件，证明 A 正定。对任意非零向量 \(x \in \mathbf{R}^{n} \)，考虑：\( x^TAx = x^T(\sum_{i=1}^n b_i b_i^T)x = \sum_{i=1}^n (x^Tb_i)(b_i^Tx) = \sum_{i=1}^n (b_i^Tx)^2 \).
记 \(B = [b_1, b_2, ..., b_n]\)，则：\( B^Tx = [b_1^Tx, b_2^Tx, ..., b_n^Tx]^T \).
由于 \(\text{rank}(B) = n\)，\(B^T\) 是满秩的，所以：
* \(x ≠ 0\) 时，\(B^Tx\) ≠ 0
* 因此 \(\sum_{i=1}^n (b_i^Tx)^2 > 0\)
因此对任意非零向量 x，都有 \(x^TAx > 0\)，即 A 正定



#### 证明 3°
从对称性 \( A = -A^T \) 出发，取特征值方程 \( Ax = \lambda x \)，两边取转置得：\((Ax)^T = (\lambda x)^T\)
展开左边和右边：  
\( (Ax)^T = x^T A^T \)  
\( (\lambda x)^T = \lambda x^T \) （因为 \( \lambda \) 是标量）  

因此：  \(x^T A^T = \lambda x^T\)
因为 \( A = -A^T \)，所以 \( A^T = -A \)，代入得到：\(x^T (-A) = \lambda x^T \implies -x^T A = \lambda x^T\)
将原方程 \( x^T A = \lambda x^T \) 与此式比较，得：\(\lambda = -\lambda\)
这说明 \( \lambda \) 满足：\(\lambda + \lambda = 0 \Longrightarrow \lambda = 0 \quad \text{或} \quad \lambda = \text{纯虚数}\)
考虑 A 的复数特征值
如果 λ 是非零特征值，则 -λ 也是特征值
纯虚数特征值总是成对出现（共轭成对）
设 A 的秩为 r，r 就是非零特征值的个数，这些非零特征值必须成对出现


#### 证明 5°
对于一个形如如下的分块矩阵：\(A = \begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22}
\end{pmatrix}\)
其中，\( A_{11}, A_{12}, A_{21}, A_{22} \) 都是矩阵块，矩阵 \( A_{11} \) 和 \( A_{22} \) 是方阵，行列式的计算公式如下：
\[
\det(A) = \det(A_{11}) \cdot \det(A_{22} - A_{21} A_{11}^{-1} A_{12})
\]

要求 \( A_{11} \) 是可逆矩阵，即它的行列式非零，并且需要计算 \( A_{11}^{-1} \)。

第一步：验证 \( f(x) \) 是二次型
首先注意到矩阵 \( \begin{bmatrix} A & x \\ x^T & 0 \end{bmatrix} \) 是 \( (n+1) \times (n+1) \) 矩阵。根据分块矩阵行列式计算公式：

\[
f(x) = \det\begin{bmatrix} A & x \\ x^T & 0 \end{bmatrix} = \det(A) \cdot \det(0 - x^T A^{-1} x)
\]

\[
= \det(A) \cdot (-x^T A^{-1} x)
\]

这表明 \( f(x) \) 是 \( x \) 的二次型。

第二步：证明 \( f(x) \) 是负定的
由于 \( A \) 正定，所以：\( \det(A) > 0 \)、\( A^{-1} \) 也正定

对于任意非零向量 \( x \in \mathbf{R}^n \)：
\( x^T A^{-1} x > 0 \)（因为 \( A^{-1} \) 正定）、所以 \( -x^T A^{-1} x < 0 \)

因此：\(
f(x) = \det(A) \cdot (-x^T A^{-1} x) < 0, \quad \text{对所有 } x \neq 0 \text{ 成立}
\)
当 \( x = 0 \) 时，显然 \( f(0) = 0 \)。

---

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

---

### V 证明以下各题
6° 设 \( B = \begin{pmatrix} \alpha & a^H \\ a & A \end{pmatrix} \)，其中 \( A \in \mathbf{C}^{n \times n} \)，且 \( A = A^H \)，即 \( A \) 为赫尔米特矩阵，\( a \in \mathbf{C}^n \)，则证明：在复平面上，存在特征值 \( \lambda \) 满足：\(
|\lambda - \alpha| \leqslant (a^H a)^{\frac{1}{2}}
\)

#### 证明 6°
首先，由于矩阵 B 是赫尔米特矩阵(因为 \(A=A^H\) 且整个矩阵 B 的结构是赫尔米特的)，所以它的所有特征值都是实数。
设 \(λ\) 是矩阵 B 的任意特征值，对应的特征向量为 \( x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} \)，其中 \(x₁\)是复数，\(x₂\) 是 n 维复向量。
由特征值方程：\( Bx = λx \) 可得：\(\begin{pmatrix} \alpha & a^H \\ a & A \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = λ\begin{pmatrix} x_1 \\ x_2 \end{pmatrix} \)
展开得到方程组：
\( \alpha x_1 + a^H x_2 = λx_1 \)
\( ax_1 + Ax_2 = λx_2 \)
假设 \(x₁ ≠ 0\) (如果 \(x₁ = 0\)，可以通过其他方法证明)。
从第一个方程得到：
\( (λ - \alpha)x_1 = a^H x_2 \)
从第二个方程得到：
\( ax_1 + (A - λI)x_2 = 0 \)
\( x_2 = -(A - λI)^{-1}ax_1 \)（假设 \(λ\) 不是 A 的特征值）
代入第一个方程：\( (λ - \alpha)x_1 = -a^H(A - λI)^{-1}ax_1 \)
消去 \(x₁\)：\( λ - \alpha = -a^H(A - λI)^{-1}a \)
根据算子范数的性质：\( |λ - \alpha| = |a^H(A - λI)^{-1}a| \leq \|a^H\| \|(A - λI)^{-1}\| \|a\| = (a^H a)^{\frac{1}{2}} \|(A - λI)^{-1}\| \|a\| = a^H a \|(A - λI)^{-1}\| \)
由于 B 是赫尔米特矩阵，必然存在至少一个特征值 λ 使得上述不等式成立，且：\( |λ - \alpha| \leq (a^H a)^{\frac{1}{2}} \)
因此，在复平面上存在特征值 \(λ\) 满足：\( |λ - \alpha| \leq (a^H a)^{\frac{1}{2}} \)


