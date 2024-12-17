## 第一章

### I 判断下述集合是否为线性空间
2° 在区间 \( \alpha \leqslant \tau \leqslant \beta \) 上满足 \( |f(\tau)| \leqslant M \) 的实值函数 \( f(\tau) \) 的全体，其中 \( M \) 为一正实数。

5° \( \mathrm{M} = \{ x \mid \dot{x} = Ax, \, A \in \mathbf{C}^{n \times n} \} \), \( \dot{x} = \dfrac{dx}{d\tau} \)。


#### 证明 2°
集合 \( S = \{ f(\tau) \mid |f(\tau)| \leq M, \, \tau \in [a, b] \} \)。  
考虑加法封闭性：设 \( f(\tau) \in S, \, g(\tau) \in S \)。  
\(|f(\tau)| \leq M, \, |g(\tau)| \leq M\)。  
\(|f(\tau) + g(\tau)| \leq |f(\tau)| + |g(\tau)| \leq 2M\)。  
因此加法不封闭，\( S \) 不是线性空间。


#### 证明 5°
\( M = \{ x \mid \dot{x} = Ax, \, A \in \mathbf{C}^{n \times n} \}, \quad \dot{x} = \dfrac{dx}{dt} \)。  
考虑加法封闭性：\( x_1 \in M, \, x_2 \in M \)，则 \( x_1 = Ax_1, \, x_2 = Ax_2 \)。  
\(
\dfrac{d(x_1 + x_2)}{dt} = \dfrac{dx_1}{dt} + \dfrac{dx_2}{dt} = Ax_1 + Ax_2 = A(x_1 + x_2),
\)满足加法封闭性。  

考虑数乘封闭性：  
\(
\dfrac{d(cx)}{dt} = c \dfrac{dx}{dt} = cAx = A(cx),
\) 也满足数乘封闭性。  
零向量：\( 0 \) 满足 \( 0 = A \cdot 0 = 0 \)，因此 \( 0 \in M \)。  综上，\( M \) 是线性空间。

---

### III 证明下述结论

2° \( \mathbf{U}_i \subset \mathbf{S}, \, i \in \{ 1, 2 \} \) 是 \( \mathbf{S} \) 的真子空间，则存在 \( a \in \mathbf{S} \)，但 \( a \notin \mathbf{U}_i \, (i \in \{ 1, 2 \}) \)，其中 \( \mathbf{S} \) 是线性空间。

#### 证明 2°
1°  \( U_{1} \subset U_{2} \) 或 \( U_{2} \subset U_{1} \)，则 \( U_{1} \cup U_{2} = U_{1} \) 或 \( U_{2} \subsetneqq S \)，符合。  
2°  \( U_{1} \not\subset U_{2} \) 且 \( U_{2} \not\subset U_{1} \)，即存在 \( a_1 \in U_1 \)，\( a_1 \notin U_2 \)，且 \( a_2 \in U_2 \)，\( a_2 \notin U_1 \)。  
由于 \( a_1, a_2 \in S \)，而 \( S \) 为线性空间，故 \( a_1 + a_2 \in S \)。  
若能证明 \( U_1 \cup U_2 \neq S \)，也就能找到不属于 \( U_1 \) 和 \( U_2 \) 的元素满足题目要求。  
下面使用反证法：  
设 \( S = U_1 \cup U_2 \)，则 \( a_1 + a_2 \in U_1 \) 或 \( U_2 \)。  
若 \( a_1 + a_2 \in U_1 \)，注意到 \( a_1 \in U_1 \)，而 \( U_1 \) 为 \( S \) 的子空间，故 \( a_2 = (a_1 + a_2) + (-a_1) \in U_1 \)，矛盾。  
若 \( a_1 + a_2 \in U_2 \)，同理矛盾。  
因此 \( S \neq U_1 \cup U_2 \)，所以 \( U_1 \cup U_2 \subsetneq S \)。  
由此可知，存在 \( a \in S \)，但 \( a \notin U_1 \cup U_2 \)。  
一种几何解释：\( S \) 为平面，\( U_1 \) 和 \( U_2 \) 是横轴和纵轴。

---

### IV 证明下述结论
1°  \( \mathbf{R}(A + B) \subset \mathbf{R}(A) + \mathbf{R}(B) \).  
2°  \( \mathbf{N}(A) \cap \mathbf{N}(B) = \mathbf{N}(A + B) \cap \mathbf{N}(A - B) \).  
3°  \( \text{rank}(A + B) \leq \text{rank}(A) + \text{rank}(B) \)，并举例说明该结论的等号与不等号均可能实现。  
以上 1°-3°，设 \( A \) 与 \( B \) 是同行列数的。  
4°  \( A, B \in \mathbf{C}^{n \times n} \)，若 \( AB = 0 \)，则 \( \text{rank}(A) + \text{rank}(B) \leq n \).  
5°  \( A \in \mathbf{C}^{n \times n} \)，则 \( \text{rank}(A) = 1 \) 当且仅当存在 \( a, b \in \mathbf{C}^n \) 均非零，使得 \( A = ab^T \).  
6°  \( A, B \in \mathbf{C}^{n \times n} \)，则 \( | \text{rank}(A) - \text{rank}(B) | \leq \text{rank}(A + B) \).


#### 证明 1°
取 \( x \in \mathbf{R}(A + B) \)。则有 \( y \) 使得 \( x = (A + B)y = Ay + By \in \mathbf{R}(A) + \mathbf{R}(B) \)。证毕。


#### 证明 2°

\( x \in \mathbf{N}(A) \cap \mathbf{N}(B) \)  
\(\iff Ax = 0 \) 且 \( Bx = 0 \)  
\(\implies (A + B)x = 0, \, (A - B)x = 0 \)  
\(\implies x \in \mathbf{N}(A + B) \cap \mathbf{N}(A - B) \)  
因此 \( \mathbf{N}(A) \cap \mathbf{N}(B) \subset \mathbf{N}(A + B) \cap \mathbf{N}(A - B) \).  
反之，若 \( x \in \mathbf{N}(A + B) \cap \mathbf{N}(A - B) \),  
\(\iff (A + B)x = 0 \) 且 \( (A - B)x = 0 \),  
两式相加得 \( 2Ax = 0 \implies Ax = 0 \implies x \in \mathbf{N}(A), \)  
两式相减得 \( 2Bx = 0 \implies Bx = 0 \implies x \in \mathbf{N}(B), \)  
因此 \( x \in \mathbf{N}(A) \cap \mathbf{N}(B) \).  
故 \( \mathbf{N}(A + B) \cap \mathbf{N}(A - B) \subset \mathbf{N}(A) \cap \mathbf{N}(B) \).  
综上， \( \mathbf{N}(A) \cap \mathbf{N}(B) = \mathbf{N}(A + B) \cap \mathbf{N}(A - B) \).


#### 证明 3°
1. 几何法:  
\(\text{rank}(A + B) = \dim \mathbf{R}(A + B),\)  
\(\text{rank}(A) = \dim \mathbf{R}(A),\)  
\(\text{rank}(B) = \dim \mathbf{R}(B).\)

2. 代数法:

3. 技巧法:  
注意到： \( A + B = 
\begin{pmatrix}
I_n & I_n
\end{pmatrix}
\begin{pmatrix}
A & 0 \\ 
0 & B
\end{pmatrix}
\begin{pmatrix}
I_n \\ 
I_n
\end{pmatrix}, \)  
故 \( \text{rank}(A + B) \leq \text{rank}
\begin{pmatrix}
A & 0 \\ 
0 & B
\end{pmatrix}, \)  
= \( \text{rank}(A) + \text{rank}(B). \)




#### 证明 4°


1. 几何法：  
\( AB = 0, \)  
故 \( \mathbf{R}(B) \subset \mathbf{N}(A), \)  
\( \dim \mathbf{R}(A) + \dim \mathbf{N}(A) = n, \)  
\(\geq \dim \mathbf{R}(A) + \dim \mathbf{R}(B) = \operatorname{rank}(A) + \operatorname{rank}(B). \)  
证毕.

2. 代数法：  
设 \( \operatorname{rank}(A) = r_A \)，存在可逆矩阵 \( P, Q \)，使得\( Q^{-1} B = 
\begin{pmatrix}
I_m & 0 \\
0 & 0
\end{pmatrix}, \, B \in \mathbf{C}^{n \times n}. \)  
\( O = PAB, \)  
\(
= 
\begin{pmatrix}
I_{r_A} & 0 \\
0 & 0
\end{pmatrix}
\begin{pmatrix}
B_1 \\
B_2
\end{pmatrix}, \quad \text{即 } B_1 = 0. \)  
故 \( r_B = \operatorname{rank}(B) = \operatorname{rank}(Q^{-1} B) = 
\text{rank}
\begin{pmatrix}
0 \\
B_2
\end{pmatrix} \leq n - r_A. \)  
因此 \( r_A + r_B \leq r_A + (n - r_A) = n. \)证毕.

#### 证明 5°
1. 代数法  
令 \( P, Q \) 可逆，使得 \( PAQ = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}_{(n-1) \times (n-1)}  
= \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix} (1\ 0\cdots0), \)  
故 \( A = [P^{-1} \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix}] [ (1 \ 0\cdots0) Q^{-1}]  
= ab^T, \)  
其中 \( a \) 为 \( P^{-1} \) 的第 1 列，\( b^T \) 为 \( Q^{-1} \) 的第 1 行，显然，\( a, b \neq 0 \)，证毕.

2. 几何法  
\( \operatorname{rank}(A) = 1, \) 即 \( A = [a_1 \ldots a_n], \, a_i \in \mathbf{C}^n, 1 \le i \le n \)  
\( \dim \mathbf{R}(A) = 1, \) 即 \( a_k \) 为 \( \mathbf{R}(A) \) 的一组基,  
不妨设 \( k = 1, \) 即有 \( \alpha_i \) 使得 \( a_i = \alpha_i \cdot a_1, i=2, \cdots,n \)  
故 \( A = [a_1\quad \alpha_1 \cdot a_1 \, \ldots \, \alpha_n\cdot a_1], \)  
\( = a_1 \begin{pmatrix} 1 & \alpha_1 & \cdots & \alpha_n \end{pmatrix}, \)  
令 \( a = a_1, \, b^T = (1, \alpha_1, \cdots, \alpha_n), \) 显然 \( a \neq 0 \)（基向量不为0），\( b \neq 0, \quad \) 证毕.



#### 证明 6°
原式等价于证明如下两个不等式（绝对值打开）：  
\(\operatorname{rank}(A) \leq \operatorname{rank}(A + B) + \operatorname{rank}(B),\)  
\(\operatorname{rank}(B) \leq \operatorname{rank}(A + B) + \operatorname{rank}(A),\)  
注意到 \( A = (A + B) + (-B), \) 且 \( \operatorname{rank}(B) = \operatorname{rank}(-B), \)  
利用第3题结论，得到  
\(\operatorname{rank}(A) \leq \operatorname{rank}(A + B) + \operatorname{rank}(-B),\)  
\(\operatorname{rank}(A) \leq \operatorname{rank}(A + B) + \operatorname{rank}(B), \) 同理可证另外一个.

---

### V 证明下述结论
1° \( A \in \mathbf{C}^{m \times n} \), 则有 \( \mathbf{R}(A) = \mathbf{R}(AA^H), \quad \mathbf{N}(A) = \mathbf{N}(A^H A). \)  

2° \( A \in \mathbf{C}^{m \times n} \), 则 \( A^H A \text{ 可逆当且仅当 } \operatorname{rank}(A) = n, \, AA^H \text{ 可逆当且仅当 } \operatorname{rank}(A) = m. \)  

3° \( A \in \mathbf{C}^{m \times n}, \, B \in \mathbf{C}^{n \times l} \), 则 \( \operatorname{rank}(AB) = \operatorname{rank}(B) - \dim[\mathbf{N}(A) \cap \mathbf{R}(B)]. \)  

4° \( A \in \mathbf{C}^{n \times n} \) 且 \( A^2 = I_n \), 则 \( \operatorname{rank}(A + I_n) + \operatorname{rank}(A - I_n) = n. \)  


#### 证明 1°

显然有\(\mathbf{R}(AA^H) \subseteq \mathbf{R}(A),\) (1)  
\(\mathbf{N}(A) \subseteq \mathbf{N}(A^H A),\) (2)  
下证反包含关系或维数相等：  

对于 (2)，反包含关系更容易  
\(\forall x \in \mathbf{N}(A^H A), \, \text{有 } A^H A x = 0,\)  
\(\Rightarrow x^H A^H A x = 0, \, \text{则 } (Ax)^H (Ax) = 0,\)  
\(\Rightarrow Ax = 0 \, \Rightarrow x \in \mathbf{N}(A),\)  
从而 \(\mathbf{N}(A^H A) \subseteq \mathbf{N}(A),\) 因此 \(\mathbf{N}(A) = \mathbf{N}(A^H A),\) (3)  

对于 (1)，维数更容易证明。  
有 \(\dim \mathbf{R}(A^H A) = n - \dim \mathbf{N}(A A^H)\)  
\(= n - \dim \mathbf{N}(A^H), \quad \text{由 (3) 得到}\)  
\(= \dim \mathbf{R}(A^H) = \operatorname{rank}(A^H) = \operatorname{rank}(A) = \dim \mathbf{R}(A),\) (4)  
于是 \(\mathbf{R}(AA^H) = \mathbf{R}(A).\) 由 (1)(4) 得到

#### 证明 2° 推论
\(\operatorname{rank}(A^H) = \operatorname{rank}(A) = \operatorname{rank}(A^H) = \operatorname{rank}(A^H A).\)  
\(A x = b\) 最小二乘法 \(\|A x - b\|_2 = \min\) 解为 \(A^H A x = A^H b\) (一定有解)，  
因为由 1 知 \(\mathbf{R}(A^{H} A) = \mathbf{R}(A^{H}),\)  
\(\forall b \in \mathbf{R}^n, \, A^{H} b \in \mathbf{R}(A^{H}) = \mathbf{R}(A^{H} A),\) 故 \(A^{H} A x = A^{H} b\) 对 \(\forall b\) 有解。  


#### 证明 3°
\(\operatorname{rank}(AB) = \dim(\mathbf{R}(AB))\)  
\(= \dim(A \cdot \mathbf{R}(B))\)  
令 \(V = \mathbf{R}(B)\)，根据定理 1.8.2 得证，见书上 \(P_{26}\)。  

#### 定理 1.8.2
\(\sigma, \mathbf{S}, \mathbf{T}, \mathbf{Q}, \mathbf{U}\) 如定义 1.8.2，则：  

1° \(\dim[\sigma(\mathbf{Q})] = \dim(\mathbf{Q}) - \dim[\mathbf{Q} \cap \mathrm{Ker}(\sigma)]\),  
2° \(\dim[\sigma^{-1}(\mathbf{U})] = \dim[\mathrm{Ker}(\sigma)] + \dim[\mathbf{U} \cap \mathrm{Im}(\sigma)]\),  
3° \(\dim(\mathbf{S}) = \dim[\mathrm{Ker}(\sigma)] + \dim[\mathrm{Im}(\sigma)]\).  

#### 证明 4°
\(A^2 = I_n \Rightarrow A^2 = I_n^2,\)  
\(\Rightarrow (A + I_n)(A - I_n) = 0,\)  
\(r(A + I_n) + r(A - I_n) \leq n \, (\text{由 IV 4 知}).\)  
下证反方向：
\(n = \operatorname{rank}(2I_n),\)  
\(= \operatorname{rank}[(A + I_n) + (-A + I_n)],\)  
\(\leq \operatorname{rank}(A + I_n) + \operatorname{rank}(-A + I_n),\)  
\(= \operatorname{rank}(A + I_n) + \operatorname{rank}(A - I_n).\)  

---

### 补充

例1  \(
\operatorname{rank}(A|B) \leq \operatorname{rank}(A) + \operatorname{rank}(B)\) 

例2 \(
\operatorname{rank}(AB) \leq \min\{\operatorname{rank}(A), \operatorname{rank}(B)\}\) 


#### 证明 例1
\((A \mid B) = (A \mid O) + (O \mid B)\)，  
因此 \(\operatorname{rank}(A \mid B) \leq \operatorname{rank}(A) + \operatorname{rank}(B)\)。  证毕。

#### 证明 例2
\(\mathbf{R}(AB) \subseteq \mathbf{R}(A)\)，\(\mathbf{R}(B^T A^T) \subseteq \mathbf{R}(B^T)\)，  
因此，\(\operatorname{rank}(AB) = \dim \mathbf{R}(AB) \leq \dim \mathbf{R}(A) = \operatorname{rank}(A)\)，  
\(\operatorname{rank}(AB) = \operatorname{rank}((AB)^T) = \operatorname{rank}(B^T A^T) \leq \dim \mathbf{R}(B^T) = \operatorname{rank}(B)\)。

