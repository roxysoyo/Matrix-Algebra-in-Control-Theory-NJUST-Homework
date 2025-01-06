## 第三章

### I 证明下述结论

1° \( A \in \mathbf{C}^{n \times n} \)，若对任何 \( X \in \mathbf{C}^{n \times n} \) 都有 \( AX = XA \)，则 \( A = \lambda I_n, \, \lambda \in \mathbf{C} \).

2° \( A \in \mathbf{C}^{n \times n} \)，则存在 \( B \in \mathbf{C}^{n \times n} \) 使得 \( AB = 0 \) 且有  
 \[
\operatorname{rank}(A) + \operatorname{rank}(B) = n.
\]

3° \( A \in \mathbf{C}^{n \times n} \)，则 \( A \) 的特征值全为零当且仅当存在 \( k \leqslant n \) 使得 \( A^k = 0 \).

4° 若 \( A^2 = A \in \mathbf{C}^{n \times n} \)，则 \( A \) 的特征值非 1 即 0.

5° 设 \( A \in \mathbf{C}^{n \times n} \) 且 \( A^2 = A \)（幂等矩阵），则存在 \( X \in \mathbf{C}_n^{n \times n} \) 使得 \(X^{-1} A X = \begin{bmatrix} I_r & 0 \\ 0 & 0 \end{bmatrix}, r = \mathrm{rank}(A).\)

---

#### 证明 1°
==法 1. 常规证法==
充分利用任意性取特殊 \( X \) 即可。取 \( X = \begin{pmatrix} 0 & \cdots & 0 & \cdots & 0 \\ 0 & \cdots & 0 & \cdots & 0 \\ \vdots & & \vdots & & \vdots \\ 0 & \cdots & 1 & \cdots & 0 \\ \vdots & & \vdots & & \vdots \\ 0 & \cdots & 0 & \cdots & 0 \end{pmatrix},  \) \( x_{ij} = 1\), 其余元素为0. 计算： \( AX = \begin{pmatrix} 0 & \cdots & a_{1j} & \cdots & 0 \\ \vdots & & \vdots & & \vdots \\ 0 & \cdots & a_{nj} & \cdots & 0 \end{pmatrix}, \quad XA = \begin{pmatrix} 0 & \cdots & 0 \\ \vdots & & \vdots \\ a_{i1} & \cdots & a_{in} \\ \vdots & & \vdots \\ 0 & \cdots & 0 \end{pmatrix}. \) 由 \( AX = XA \)，可得 \( A \) 的非对角元均为 0，故 \( A \) 为对角阵。

==法 2. ==
\( \forall x \in \mathbf{C}^n, \, AXx = XAx, \quad \forall X \in \mathbf{C}^{n \times n}. \) 取 \( x = x_0 \) 为 \( A \) 对应特征值 \( \lambda \) 的特征向量，则 \( A X x_0 = X A x_0 = \lambda X x_0. \) 即 \( X \in \mathbf{C}^{n \times n}, X x_0 \neq 0, X x_0 \) 也为 \( A \) 对应 \( \lambda \) 的特征向量。由于 \( x_0 \neq 0 \)，不妨设其第一个分量 \( \xi_1 \neq 0 \)，令 \( x_0 = (\xi_1, \ldots, \xi_n)^T. \) 定义矩阵 \( X_i \) 为： \( X_i = \begin{pmatrix} 0 & \cdots & 0 \\ 1/\xi_i & \cdots & 0 \\ 0 & \cdots & 0 \end{pmatrix} \in \mathbf{C}^{n \times n}, \quad 1 \leq i < n. \) 于是 \( X_i x_0 = e_i = \begin{pmatrix} 0 \\ \vdots \\ 1 \\ \vdots \\ 0 \end{pmatrix} \)  
这里 \( e_i \) 对应第 \( i \) 个位置非零，且为 \( A \) 对应于 \( \lambda \) 的特征向量。
由此，\(A = A I_n = (A e_1, \ldots, A e_n),\)且\(A = \lambda (e_1, \ldots, e_n) = \lambda I_n.\)证毕。


#### 证明 2°
==法 1. 常规法==
令 \( b_1, \dots, b_r \) 为 \( N(A) \) 的一组基，\( B = \begin{pmatrix} b_1 & \cdots & b_r & 0 & \cdots & 0 \end{pmatrix} \in \mathbf{C}^{r \times n} \)。若 \( A B = 0 \)，则 \( \text{rank}(B) = \dim N(A) = n - \dim R(A) = n - \operatorname{rank}(A) \)。

==法 2. Jordan 标准型法==
根据Jordan标准型理论，存在可逆矩阵P，使得：\( A = PJP^{-1} \)，其中\(J\)是A的Jordan标准型。
设 \(r = rank(A)\)，则J可以写成分块对角矩阵的形式：
\[ J = \begin{bmatrix} J_r & 0 \\ 0 & 0_{n-r} \end{bmatrix} \]
其中\(J_r\)是\(r×r\)的非奇异Jordan块，\(0_{n-r}\)是\((n-r)×(n-r)\)的零矩阵。
可以构造矩阵B'如下：
\[ B' = \begin{bmatrix} 0_r & 0 \\ 0 & I_{n-r} \end{bmatrix} \]
其中\(I_{n-r}\)是(n-r)×(n-r)的单位矩阵。
验证JB' = 0
\[ JB' = \begin{bmatrix} J_r & 0 \\ 0 & 0_{n-r} \end{bmatrix} \begin{bmatrix} 0_r & 0 \\ 0 & I_{n-r} \end{bmatrix} = 0 \]
定义矩阵B
\[ B = P B' P^{-1} \]
验证AB = 0
\[ AB = (PJP^{-1})(PB'P^{-1}) = P(JB')P^{-1} = 0 \]

\(rank(B) = rank(B') = n-r\) （因为相似变换不改变秩）
\(rank(A) = r\)
因此 \(rank(A) + rank(B) = r + (n-r) = n\)

#### 证明 3°
Jordan 标准型法
充分性（⇐）
假设存在 \( k \leqslant n \) 使得 \( A^k = 0 \)

设 λ 是 A 的任意特征值，x 是对应的特征向量，则：\( Ax = λx \)
由此可得：\( A^kx = λ^kx \)
又因为 \( A^k = 0 \)，所以：\( 0 = A^kx = λ^kx \)
因为 \(x ≠ 0\)（特征向量非零），所以必有：\( λ^k = 0 \)
即\(λ = 0\)，即 \(A\) 的所有特征值都为 0
必要性（⇒）
假设 A 的所有特征值都为 0

根据Jordan标准型理论，存在可逆矩阵 P 使得：\( A = PJP^{-1} \)，其中 J 为 A 的Jordan标准型
由于 A 的特征值全为 0，J 由若干个形如：\( J_i = \begin{bmatrix} 
0 & 1 & 0 & \cdots & 0 \\
0 & 0 & 1 & \cdots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \cdots & 1 \\
0 & 0 & 0 & \cdots & 0
\end{bmatrix} \)的Jordan块组成
每个 \(m_i \times m_i\) 的Jordan块 \(J_i\) 在 \(m_i\) 次幂后变为零矩阵
令 \(k\) 为最大的Jordan块大小，则 \(k ≤ n\)，且：\( J^k = 0 \)
因此：\( A^k = (PJP^{-1})^k = PJ^kP^{-1} = 0 \)


#### 证明 4°
设 \( x_0 \) 为 \( A \) 对应的特征向量，\( A x_0 = \lambda x_0, \, x_0 \neq 0 \)。由此得 \( A^2 x_0 = \lambda A x_0 = \lambda^2 x_0, \, x_0 \neq 0 \)。故 \( \lambda x_0 = \lambda^2 x_0 \)。于是 \((\lambda^2 - \lambda) x_0 = 0 \Rightarrow \lambda^2 - \lambda = 0 \)，即 \( \lambda = 0 \) 或 \( \lambda = 1 \)。

#### 证明 5°
==法 1. 常规做法==
\( A^2 = A \)，即矩阵 \( A \) 的特征值为 \( 0 \) 或 \( 1 \)。  
原式等价于 \( AX = X \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix} \)，即找一组基底 \( X \)，使 \( A \) 在 \( X \) 下表示为  \(\begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix}.\) 设 \( X = (x_1, \ldots, x_n) \)，有  \(A x_i =
\begin{cases} 
x_i, & 1 \leq i \leq r, \\
0, & r < i \leq n.
\end{cases}\) 
取 \( (x_1, \ldots, x_r) \) 为 \( R(A) \) 的一组基，当 \( R(A) + N(A) = R(A) \oplus N(A) \) 时，\( X = (x_1, \ldots, x_n) \) 可逆。  
此时\(A X = (A x_1, \ldots, A x_r, 0, \ldots, 0) = \begin{pmatrix} x_1, \ldots, x_n \end{pmatrix} \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix} = X \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix}.\) 
下证 \( R(A) + N(A) = R(A) \oplus N(A) \)。  
令 \( x \in R(A) \cap N(A), x \neq 0 \)，则存在 \( y \)，使 \( x = A y \)，且 \(A x = 0 \)。  所以  \(0 = A x = A^2 y = A y = x \neq 0,\)  矛盾。因此 \( R(A) \cap N(A) = \{0\} \)。又 \(\dim R(A) + \dim N(A) = n,\) 所以  \(\dim (R(A) + N(A)) = n.\) 因此 \(R(A) \oplus N(A) = \mathbf{C}^n.\) 

==法 2. Jordan 标准型法==
由 \( A^2 = A \)，对任意特征值 λ 和对应特征向量 v，有：\( A^2v = Av \implies λ^2v = λv \implies λ^2 = λ \)，因此 λ 只能取值 0 或 1
由Jordan标准型理论，存在可逆矩阵P使得：\( A = PJP^{-1} \)其中J是A的Jordan标准型

代入 \( A^2 = A \) 得：
\( (PJP^{-1})(PJP^{-1}) = PJP^{-1} \)
\( PJ^2P^{-1} = PJP^{-1} \)
\( J^2 = J \)，这说明每个Jordan块也必须满足幂等性

对于任意Jordan块 \( J_i \)，如果它大小大于1，即包含上三角的1，则：\[ J_i^2 \neq J_i \]这说明所有Jordan块必须是1×1的，即J是对角矩阵

由于特征值只能是0或1，所以J的形式必然是：\[ J = \begin{bmatrix} I_r & 0 \\ 0 & 0 \end{bmatrix} \]其中r是特征值1的个数
\( \mathrm{rank}(A) = \mathrm{rank}(PJP^{-1}) = \mathrm{rank}(J) = r \)
取 \( X = P \)，则：\[ X^{-1}AX = P^{-1}(PJP^{-1})P = J = \begin{bmatrix} I_r & 0 \\ 0 & 0 \end{bmatrix} \]

---

### II 证明下述结论
1° 任何 \( A \in \mathbf{C}^{m \times n}, B \in \mathbf{C}^{n \times m} \)，则 \(
\begin{bmatrix}
AB & 0 \\
B & 0
\end{bmatrix} 
\sim 
\begin{bmatrix}
0 & 0 \\
B & BA
\end{bmatrix}.
\)

2° 对任何 \( A \in \mathbf{C}^{m \times n}, B \in \mathbf{C}^{n \times m} \)，则 \( AB \) 与 \( BA \) 具相同的非零特征值。

6° \( A = aa^H \in \mathbf{C}^{n \times n} \) 的特征值是 \( 0 \) 与 \( a^H a \)。


#### 证明 1°
令 \( M = \begin{bmatrix} I_{m} & -A \\ 0 & I_{n} \end{bmatrix}, \quad M^{-1} = \begin{bmatrix} I_{m} & A \\ 0 & I_{n} \end{bmatrix} \)

\( M \begin{bmatrix} AB & 0 \\ B & 0 \end{bmatrix} M^{-1} = \begin{bmatrix} 0 & 0 \\ B & 0 \end{bmatrix} \begin{bmatrix} I_{m} & A \\ 0 & I_{n} \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ B & BA \end{bmatrix} \)


#### 证明 2°
假设 \( (\lambda \neq 0) \) 是 \( AB \) 的一个非零特征值，且对应的特征向量为 \( x \in \mathbf{C}^m \)，\( ABx = \lambda x \)。
将 \( x \) 的两边左乘 \( B \)，得到：\( B(ABx) = \lambda Bx \)，矩阵的结合律：\( (BA)(Bx) = \lambda (Bx) \)。
令 \( y = Bx \)。 如果 \( y \neq 0 \)，则上式说明 \( \lambda \) 也是 \( BA \) 的特征值。
反之，如果 \( \mu \neq 0 \) 是 \( BA \) 的一个非零特征值且对应特征向量为 \( y \in \mathbf{C}^n \)，\( BAy = \mu y \)。
将 \( y \) 的两边左乘 \( A \)，得到：\( A(BAy) = \mu Ay \)，同样，矩阵的结合律成立：\( (AB)(Ay) = \mu (Ay) \)。
令 \( z = Ay \)。 如果 \( z \neq 0 \)，则上式说明 \( \mu \) 也是 \( AB \) 的特征值。

#### 证明 6°
由 \( 2^{\circ} \) 直接得，令 \( A = a \), \( B = a^H \), \( a^H a \) 为标量，特征值为 \( a^H a \)。
