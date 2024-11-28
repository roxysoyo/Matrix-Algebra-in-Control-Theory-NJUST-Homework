# 系统与控制理论中的线性代数（上册）（第二版） 黄琳 编著

## 课堂作业

1. $S$ 为平面，$L$ 为如图所示的直线，$L = \{(\xi_1, \xi_2)^T \mid \xi_1 + \xi_2 = 1\}$，是否有可能定义 $L$ 中的加法和数量乘法，使得 $L$ 成为 $\mathbf{R}$ 上的线性空间？

2. 考虑单位圆周 $L$，是否有可能定义 $L$ 中的加法和数量乘法，使得 $L$ 成为 $\mathbf{R}$ 上的线性空间？

3. 如何定义封闭曲线 $L$ 的向量加法和数量乘法，使得 $L$ 成为 $\mathbf{R}$ 上的线性空间？若 $L'$ 为有限曲线段，又该如何定义向量加法和数量乘法呢？

4. 你是否认为真有“跳跌性思维”，即你面对一个正常人发现他的表述主题是随机跳跃的，相互之间没有规律可言？试用学过的线性代数知识解释这一现象。





## 第一章作业

### I

I. 判断下述集合是否为线性空间：

1. 在区间 $\alpha \leqslant \tau \leqslant \beta$ 上定义的可微实函数的全体。
2. 在区间 $\alpha \leqslant \tau \leqslant \beta$ 上满足 $|f(\tau)| \leqslant M$ 的实值函数 $f(\tau)$ 的全体，其中 $M$ 为一正实数。
3. $\mathrm{M} = \{ x \mid \xi_1 + \xi_2 = 0 \} \subset \mathbf{R}^n$.
4. $\mathrm{M} = \{ x \mid 2\xi_1 + 3\xi_2 = 3 \} \subset \mathbf{C}^n$.
5. $\mathrm{M} = \{ x \mid \dot{x} = Ax, \, A \in \mathbf{C}^{n \times n} \}$, $\dot{x} = \frac{dx}{d\tau}$.

证$2^{\circ}$：
$$
\begin{aligned}
&\text{集合 }S=\{f(\tau)\mid|f(\tau)|\leq M,\, \tau\in[a,b]\}\\
&\text{考虑加法封闭性:设 }f(\tau)\in S, g(\tau)\in S.\\
&|f(\tau)|\leq M, |g(\tau)|\leq M.\\
&|f(\tau)+g(\tau)|\leq|f(\tau)|+|g(\tau)|\leq 2M. \\
&\text{因此加法不封闭, }S\text{ 不是线性空间}.
\end{aligned}
$$
证$5^{\circ}$：
$$
\begin{aligned}
& M = \{x \mid \dot{x} = Ax, \, A \in \mathbf{C}^{n \times n}\}, \quad \dot{x} = \frac{dx}{dt}. \\
& \text{考虑加法封闭性:} \quad x_1 \in M, \quad x_2 \in M \text{，则 } x_1 = Ax_1, \quad x_2 = Ax_2. \\
& \frac{d(x_1 + x_2)}{dt} = \frac{dx_1}{dt} + \frac{dx_2}{dt} = Ax_1 + Ax_2 = A(x_1 + x_2), \text{满足加法封闭性}. \\
& \text{考虑数乘封闭性:} \quad \frac{d(cx)}{dt} = c \frac{dx}{dt} = cAx = A(cx), \text{也满足数乘封闭性}. \\
& \text{零向量: } 0 \text{ 满足 } 0 = A \cdot 0 = 0, \text{因此}0 \in M. \\
& \text{综上 } M \text{ 是线性空间}.
\end{aligned}
$$

### III

$1^\circ \quad \mathbf{U}_i \subset \mathbf{S},i \in \{1, 2\} \text{ 是 } \mathbf{S} \text{ 的真子空间，}
则存在a \in \mathbf{S}，但  a \notin \mathbf{U}_i, ( i \in \{1, 2\})，其中\mathbf{S}是线性空间。$

证：
$$
\begin{aligned}
& 1^{\circ} \, U_{1} \subset U_{2}\text{ 或 } U_{2} \subset  U_{1}, \\
& \text{则 } U_{1} \cup U_{2} = U_{1} \text{ 或 } U_{2} \subsetneqq S, \, \text{符合。} \\

& 2^{\circ} \, U_{1} \not\subset U_{2} \text{ 且 } U_{2} \not\subset U_{1}, \\
& \text{即存在 } a_1 \in U_1, \, a_1 \notin U_2, \, \text{且 } a_2 \in U_2, \, a_2 \notin U_1. \\
& \text{由于 } a_1, a_2 \in S, \, \text{而 } S \text{ 为线性空间，} \\
& \text{故 } a_1 + a_2 \in S. \\
& \text{若能证明 } U_1 \cup U_2 \neq S, \text{也就能找到不属于} U_1\text{和}U_2的元素满足题目要求\\

& \text{下面面使用反证法}\\
& \text{设 } S = U_1 \cup U_2, \\
& \text{则 } a_1 + a_2 \in U_1 \text{ 或 } U_2. \\
& \text{若 } a_1 + a_2 \in U_1, \text{ 注意到 } a_1 \in U_1, \text{而 } U_1 \text{ 为 } S \text{ 的子空间，} \\
& \text{故 } a_2 = (a_1 + a_2) + (-a_1) \in U_1, \text{ 矛盾。} \\
& \text{若 } a_1 + a_2 \in U_2, \text{ 同理矛盾。} \\
& \text{因此 } S \neq U_1 \cup U_2, \text{所以 } U_1 \cup U_2 \subsetneq S. \\
& \text{由此可知，存在 } a \in S, \text{但 } a \notin U_1 \cup U_2.\\
& \text{一种几何解释：S为平面，}U_1\text{和}U_2是横轴和纵轴
\end{aligned}
$$




### IV

证明下述结论：
$1^{\circ} \textbf{ R}( A+ B) \subset \mathbf{R} ( A) + \mathbf{R} ( B) .$
$2^{\circ}\textbf{ N}( A) \cap \mathbf{N} ( B) = \mathbf{N} ( A+ B) \cap \mathbf{N} ( A- B) .$
$3^{\circ}$ $rank(A+B)\leq rank(A)+rank(B)$，并举例说明该结论的等号与不等号均可能实现.

以上$1^{\circ}-3^{\circ}$设$A$与$B$是同行列数的.

$4^{\circ}A,B\in\mathbf{C}^{n\times n},AB=0$，则 $rank(A)+rank(B)\leq n$.

$5^{\circ}A\in\mathbf{C}^{n\times n}$，则 $rank(A)=1$当且仅当有$a,b\in\mathbf{C}^n$均非零，使$A=ab^T$.
$6^{\circ}$$A, B\in \mathbf{C} ^{n\times n}$，则 $|rank(A)-rank(B)|\leq rank(A+B)$.



* 证$1^{\circ}$：

$$
\begin{aligned}
&取x\in R(A+B).\\
&则有y使x=(A+B)y=Ay+By\in R(A)+R(B).\\
&\text{证毕}
\end{aligned}
$$

* 证$2^{\circ}$：

$$
\begin{aligned}
&x \in N(A) \cap N(B) \\
&\iff Ax = 0 \text{ 且 } Bx = 0 \\
&\implies (A + B)x = 0, \, (A - B)x = 0 \\
&\implies x \in N(A + B) \cap N(A - B) \\
&\text{因此 } N(A) \cap N(B) \subset N(A + B) \cap N(A - B). \\
&\text{反之，若 } x \in N(A + B) \cap N(A - B), \\
&\iff (A + B)x = 0 \text{ 且 } (A - B)x = 0, \\
&\text{两式相加得 } 2Ax = 0 \implies Ax = 0 \implies x \in N(A), \\
&\text{两式相减得 } 2Bx = 0 \implies Bx = 0 \implies x \in N(B), \\
&\text{因此 } x \in N(A) \cap N(B). \\
&\text{故 } N(A + B) \cap N(A - B) \subset N(A) \cap N(B). \\
&\text{综上， } N(A) \cap N(B) = N(A + B) \cap N(A - B).
\end{aligned}
$$

* 证$3^{\circ}$：

$$
\begin{aligned}
&\text{1.几何法:} \\
&\text{rank}(A + B) = \dim R(A + B), \\
&\text{rank}(A) = \dim R(A), \\
&\text{rank}(B) = \dim R(B). \\

&\text{2.代数法:} \\

\end{aligned}
\begin{aligned}
&\text{3.技巧法:} \\
&\text{注意到：}
A + B = 
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
\end{pmatrix}, \\
&\text{故} \text{rank}(A + B) \leq \text{rank}
\begin{pmatrix}
A & 0 \\
0 & B
\end{pmatrix}, \\
&= \text{rank}(A) + \text{rank}(B).

\end{aligned}
$$



* 证$4^{\circ}$：

$$
\begin{aligned}
&\text{1. 几何法：} \\
&AB = 0, \\
&\text{故 } R(B) \subset N(A), \\
&\dim R(A) + \dim N(A) = n, \\
&\geq \dim R(A) + \dim R(B) = \operatorname{rank}(A) + \operatorname{rank}(B). \\
&\text{证毕}. \\
\end{aligned}


\begin{aligned}
&\text{2. 代数法：} \\
&\text{设 } \operatorname{rank}(A) = r_A, \text{ 存在可逆矩阵 } P, Q, \text{ 使 } \\
&Q^{-1} B = 
\begin{pmatrix}
I_m & 0 \\
0 & 0
\end{pmatrix}, \quad B \in \mathbb{C}^{n \times n}. \\
&O = PAB, \\
&\quad = 
\begin{pmatrix}
I_{r_A} & 0 \\
0 & 0
\end{pmatrix}
\begin{pmatrix}
B_1 \\
B_2
\end{pmatrix}, \quad \text{即 } B_1 = 0. \\
&\text{故 } r_B = \operatorname{rank}(B) = \operatorname{rank}(Q^{-1} B) = 
\text{rank}
\begin{pmatrix}
0 \\
B_2
\end{pmatrix}\leq n - r_A. \\
&\text{因此 } r_A + r_B \leq r_A + (n - r_A) = n. \\
&\text{证毕}.
\end{aligned}
$$

* 证$5^{\circ}$：

$$
\begin{aligned}
&\text{1.代数法}\\
&\text{令 } P, Q \text{ 可逆，使得} \\
& PAQ = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}_{(n-1) \times (n-1)}
= \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix} (1\ 0\cdots0), \\
&\text{故} \quad A = [P^{-1} \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix}] [ (1 \ 0\cdots0) Q^{-1}]
= ab^T, \\
&\text{其中 } a \text{ 为 } P^{-1} \text{ 的第 1 列，} b^T \text{ 为 } Q^{-1} \text{ 的第 1 行，}
\text{显然，} a, b \neq 0, \text{证毕}.
\end{aligned}


\begin{aligned}
&\text{2.几何法}\\
&\operatorname{rank}(A) = 1,\text{ 即 } A = [a_1 \ldots a_n], \, a_i \in \mathbb{C}^n, 1 \le i \le n\\
&\dim R(A) = 1, \text{ 即 } a_k \text{ 为 } R(A) \text{ 的一组基}, \\
&\text{不妨设 } k = 1, \text{ 即有 } \alpha_i \text{ 使得 } a_i = \alpha_i \cdot a_1, i=2, \cdots,n \\
&\text{故 } A = [a_1\quad \alpha_1 \cdot a_1 \, \ldots \, \alpha_n\cdot a_1], \\
&= a_1 \begin{pmatrix} 1 & \alpha_1 & \cdots & \alpha_n \end{pmatrix}, \\
&\text{令 } a = a_1, \, b^T = (1, \alpha_1, \cdots, \alpha_n), \\
&\text{显然 } a \neq 0(\text{基向量不为0}), \, b \neq 0, \quad \text{证毕}. \\
\end{aligned}
$$



* 证$6^{\circ}$：


$$
\begin{aligned}
& \text{原式等价于证明如下两个不等式 (绝对值打开)} \\
& \operatorname{rank}(A) \leq \operatorname{rank}(A + B) + \operatorname{rank}(B), \\
& \operatorname{rank}(B) \leq \operatorname{rank}(A + B) + \operatorname{rank}(A), \\
& \text{注意到 } A = (A + B) + (-B), \text{ 且 } \operatorname{rank}(B) = \operatorname{rank}(-B), \\
& \text{利用第3题结论, 得到} \\
& \operatorname{rank}(A) \leq \operatorname{rank}(A + B) + \operatorname{rank}(-B), \\
& \operatorname{rank}(A) \leq \operatorname{rank}(A + B) + \operatorname{rank}(B), \text{ 同理可证另外一个} \\
\end{aligned}
$$


### V

证明下述结论：

$1^{\circ} A \in \mathbf{C}^{m \times n}$, 则有 $ \mathbf{R}(A) = \mathbf{R}(AA^H), \quad \mathbf{N}(A) = \mathbf{N}(A^H A)$.

$2^{\circ}A \in \mathbf{C}^{m \times n}$, 则 $ A^H A \text{ 可逆当且仅当 } \operatorname{rank}(A) = n, \, AA^H \text{ 可逆当且仅当 } \operatorname{rank}(A) = m$.

$3^{\circ}A \in \mathbf{C}^{m \times n}$, $B \in \mathbf{C}^{n \times l}$, 则$ \operatorname{rank}(AB) = \operatorname{rank}(B) - \dim[\mathbf{N}(A) \cap \mathbf{R}(B)]$.  

$4^{\circ}A \in \mathbf{C}^{n \times n}$ 且 $A^2 = I_n$, 则$ \operatorname{rank}(A + I_n) + \operatorname{rank}(A - I_n) = n$.  

* 证$1^{\circ}$：

$$
\begin{aligned}
& \text{显然有} \\
& \mathbf{R}(AA^H) \subseteq \mathbf{R}(A), \text{(1)}\\
& \mathbf{N}(A) \subseteq \mathbf{N}(A^H A), \text{(2)}\\
& \text{下证反包含关系或维数相等：} \\
& \text{对于(2),反包含关系更容易} \\
\\
& \forall x \in \mathbf{N}(A^H A), \, \text{有} A^H A x = 0, \\
& \quad \Rightarrow x^H A^H A x = 0, \, \text{则}(Ax)^H (Ax) = 0, \\
& \quad \Rightarrow Ax = 0 \, \Rightarrow x \in \mathbf{N}(A), \\
& \quad \text{从而} \quad \mathbf{N}(A^H A) \subseteq \mathbf{N}(A), \\
& \text{因此} \quad \mathbf{N}(A) = \mathbf{N}(A^H A) \quad \text{(3)}. \\
\\
& \text{对于(1)维数更容易证明。} \\
& \text{有} \dim \mathbf{R}(A^H A) = n - \dim \mathbf{N}(A A^H)\\
& = n - \dim \mathbf{N}(A^H), \quad \text{由 (3) 得到} \\
& = \dim \mathbf{R}(A^H) = \operatorname{rank}(A^H) = \operatorname{rank}(A) = \dim \mathbf{R}(A) \quad \text{(4)}. \\
& \text{于是} \quad \mathbf{R}(A A^H) = \mathbf{R}(A).\text{由 (1)(4) 得到}
\end{aligned}
$$

* 证$2^{\circ}$：

$$
\begin{aligned}
& \text{推论} \quad \operatorname{rank}(A^H) = \operatorname{rank}(A) = \operatorname{rank}(A^H) = \operatorname{rank}(A^H A). \\
& A x = b \text{ 最小二乘法 }\|A x - b\|_2 = \min \text{ 解为 }A^H A x = A^H b (\text{一定有解}), \\
& \text{因为由1知} \quad \mathbf{R}(A^{H} A) = \mathbf{R}(A^{H}), \\
& \forall b \in \mathbf{R}^n, \quad A^{H} b \in \mathbf{R}(A^{H}) = \mathbf{R}(A^{H} A), \\
& \text{故} \quad A^{H} A x = A^{H} b \quad \text{对} \forall b \text{有解}.
\end{aligned}
$$





证$3^{\circ}$：
$$
\begin{aligned}
\operatorname{rank}(AB) &= \dim(\mathbf{R}(AB)) \\
&= \dim(A \cdot \mathbf{R}(B)) \\
&\text{令 } V = \mathbf{R}(B), \text{ 根据定理 1.8.2 得证.}\,\text{书上P}_{26}.
\end{aligned}
$$
定理 1.8.2
$$
&\quad \sigma, \mathbf{S}, \mathbf{T}, \mathbf{Q}, \mathbf{U} \quad \text{如定义 1.8.2, 则：}\\
&\begin{aligned}
&1^{\circ} \quad & \dim[\sigma(\mathbf{Q})] = \dim(\mathbf{Q}) - \dim[\mathbf{Q} \cap \mathrm{Ker}(\sigma)], \\
&2^{\circ} \quad & \dim[\sigma^{-1}(\mathbf{U})] = \dim[\mathrm{Ker}(\sigma)] + \dim[\mathbf{U} \cap \mathrm{Im}(\sigma)], \\
&3^{\circ} \quad & \dim(\mathbf{S}) = \dim[\mathrm{Ker}(\sigma)] + \dim[\mathrm{Im}(\sigma)].
&\end{aligned}
$$


* 证$4^{\circ}$：

$$
\begin{aligned}
A^2 &= I_n \Rightarrow A^2 = I_n^2, \\
& \Rightarrow (A + I_n)(A - I_n) = 0, \\
&r(A + I_n) + r(A - I_n) \leq n.(\text{由IV\, 4知}) \\
\text{下证反方向：} \\
& n = \operatorname{rank}(2I_n), \\
& = \operatorname{rank}[(A + I_n) + (-A + I_n)], \\
& \leq \operatorname{rank}(A + I_n) + \operatorname{rank}(-A + I_n), \\
& = \operatorname{rank}(A + I_n) + \operatorname{rank}(A - I_n).
\end{aligned}
$$



### 补充

例1：

证明：
$$
\operatorname{rank}(A|B) \leq \operatorname{rank}(A) + \operatorname{rank}(B)
$$
证：
$$
\begin{gathered}

(A|B) = (A|O) + (O|B), \\
\text{因此} \operatorname{rank}(A|B) \leq \operatorname{rank}(A) + \operatorname{rank}(B), \\
\end{gathered}
$$


例2：
$$
\operatorname{rank}(AB) \leq \min\{\operatorname{rank}(A), \operatorname{rank}(B)\}
$$
证：
$$
\mathbf{R}(AB) \subseteq \mathbf{R}(A), \\
\mathbf{R}(B^T A^T) \subseteq \mathbf{R}(B^T), \\
\text{因此}
\quad \operatorname{rank}(AB) = \dim \mathbf{R}(AB) \leq \dim \mathbf{R}(A) = \operatorname{rank}(A), \\
\operatorname{rank}(AB) = \operatorname{rank}(AB)^T = \operatorname{rank}(B^T A^T) \leq \dim \mathbf{R}(B^T)= \operatorname{rank}(B).
$$


## 第三章作业

### I

1. ${A} \in \mathbf{C}^{n \times n}$，若对任何 $X \in \mathbf{C}^{n \times n}$ 都有 $AX = XA$，则 $A = \alpha I_n, \, \alpha \in \mathbf{C}$.
2. $A \in \mathbf{C}^{n \times n}$，则存在 $B \in \mathbf{C}^{n \times n}$ 使得 $AB = 0$ 且有 $\operatorname{rank}(A) + \operatorname{rank}(B) = n$.
3. $A \in \mathbf{C}^{n \times n}$，则 $A$ 的特征值全为零当且仅当存在 $k \leqslant n$ 使得 $A^k = 0$.
4. 若 $A^2 = A \in \mathbf{C}^{n \times n}$，则 $A$ 的特征值非1即0.
5. $A \text{ 同 } 4^{\mathrm{o}}, \text{ 则存在 } X \in \mathbf{C}_n^{n \times n} \text{ 使得 } X^{-1} A X = \begin{bmatrix} I_r & 0 \\ 0 & 0 \end{bmatrix}, \text{ 其中 } r = \mathrm{rank}(A)$.

证$1^{\circ}$：

$$
\begin{aligned}
\text{证1. 常规证法} \\
&\text{充分利用任意性取特殊 } X \text{ 即可} \\
\text{取} \quad X &= \begin{pmatrix}
0 & \cdots & 0 & \cdots & 0 \\
0 & \cdots & 0 & \cdots & 0 \\
\vdots & & \vdots & & \vdots \\
0 & \cdots & 1 & \cdots & 0 \\
\vdots & & \vdots & & \vdots \\
0 & \cdots & 0 & \cdots & 0
\end{pmatrix}, \, x_{ij} = 1, \, \text{其余元素为} 0 \\
AX &= \begin{pmatrix}
0 & \cdots & a_{1j} & \cdots & 0 \\
\vdots & & \vdots & & \vdots \\
0 & \cdots & a_{nj} & \cdots & 0
\end{pmatrix}, \\
XA &= \begin{pmatrix}
0 & \cdots & 0 \\
\vdots & & \vdots \\
a_{i1} & \cdots & a_{in} \\
\vdots & & \vdots \\
0 & \cdots & 0
\end{pmatrix}, \\
AX &= XA \\
&\Rightarrow A \text{ 的非对角元均为 0}, A \text{ 为对角阵}.
\end{aligned}
\\[1em]  % 插入适当的间距

\begin{aligned}
\text{证2.} \\
& \forall x \in \mathbf{C}^n, \, AXx = XAx, \forall X \in \mathbf{C}^{n \times n}, \\
& \text{取 } x = x_0 \text{ 为 } A \text{ 对应特征值 } \alpha \text{ 的特征向量}, \\
& \text{则 } A X x_0 = X A x_0 = \alpha X x_0, \\
& \text{即} \ X \in \mathbf{C}^{n \times n}, \ X x_0 \neq 0, \ Xx_0 \text{ 也为 } A \text{ 对应 } \alpha \text{ 的特征向量}, \\
& \text{由于} x_0 \neq 0, \ \text{不妨设其第一个分量} \xi_1 \neq 0, \\
& x_0 = (\xi_1, \ldots, \xi_n)^T, \\
& \text{令} X_i = \begin{pmatrix}
0 & \cdots & 0 \\
1/\xi_i & \cdots & 0 \\
0 & \cdots & 0
\end{pmatrix} \in \mathbf{C}^{n \times n}, \, 1 \leq i < n, \\
& \text{因此} X_i x_0 = e_i = \begin{pmatrix} 0 \\ \vdots \\ 1 \\ \vdots \\ 0 \end{pmatrix} \rightarrow i \quad \text{均为 } A \text{ 对应于 } \alpha \text{ 的特征向量}, \\
& \text{故} \ A = A I_n = (A e_1, \ldots, A e_n), \\
& = \alpha (e_1, \ldots, e_n), \\
& = \alpha I_n \quad \text{证毕}.
\end{aligned}
$$


证$2^{\circ}$：
$$
\begin{aligned}
& \text{1.常规法}\\
&\text{令} \, b_1, \dots, b_r \, \text{为} \, N(A) \text{ 的一组基} \\
&B = \begin{pmatrix} b_1 & \cdots & b_r & 0 & \cdots & 0 \end{pmatrix} \in \mathbf{C}^{r \times n} \\
&\text{若} \, A B = 0, \\
&\text{则} \, \text{rank}(B) = \dim N(A) \\
&= n - \dim R(A) = n - \operatorname{rank}(A).\\
\\
& \text{2.Jordan标准型法}\\
\\
\end{aligned}
$$


证$3^{\circ}$：
$$
\begin{aligned}
& \text{Jordan标准型法}\\
\end{aligned}
$$
证$4^{\circ}$：
$$
\begin{aligned}
&\text{设 } x_0 \text{ 为 } A \text{ 对应的特征向量} \\
&A x_0 = \lambda x_0, \, x_0 \neq 0. \\
&A^2 x_0 = \lambda A x_0 = \lambda^2 x_0, \, x_0 \neq 0. \\
&\text{故 } \lambda x_0 = \lambda^2 x_0. \\
&\text{于是 } (\lambda^2 - \lambda) x_0 = 0 \Rightarrow \lambda^2 - \lambda = 0. \quad \lambda = 0 \text{ 或 } 1.
\end{aligned}
$$


证$5^{\circ}$：
$$
\begin{align*}
A^2 = A, \quad \text{即矩阵 } &A \text{ 对应的特征值为 } 0 \text{ 或 } 1. \\
\text{原式等价于}& AX = X
\begin{pmatrix}
I_r & 0 \\
0 & 0
\end{pmatrix}, \\
\text{相当于找一组基底} \, X, & \text{使得 } A \text{ 在 } X \text{ 下的矩阵表示为}
\begin{pmatrix}
I_r & 0 \\
0 & 0
\end{pmatrix}. \\

\text{设} X &= (x_1, \ldots, x_n) \\
A x_i &= \begin{cases}
x_i = (x_1, \ldots, x_n) \cdot e_i, & 1 \leq i \leq r, \\
0 = (x_1, \ldots, x_n) \cdot 0, & r < i \leq n.
\end{cases} \\

\text{取 } (x_1, \ldots, x_r) &\text{ 为 } R(A) \text{ 的一组基}, \\
\text{当 } R(A) + N(A) &= R(A) \oplus N(A) \text{ 时,} \\
X &= (x_1, \ldots, x_n) \text{ 可逆}, \\
\text{此时 } A X &= (A x_1, \ldots, A x_r, 0, \ldots, 0), \\
&= \begin{pmatrix}
x_1, \ldots, x_r, 0, \ldots, 0
\end{pmatrix}, \\
&= \begin{pmatrix} 
x_1, \ldots, x_n
\end{pmatrix}
\begin{pmatrix}
I_r & 0 \\
0 & 0
\end{pmatrix}, \\
&= X
\begin{pmatrix}
I_r & 0 \\
0 & 0
\end{pmatrix}. \\
\text{下证} \quad &R(A) + N(A) = R(A) \oplus N(A).\\

\text {令 } &x \in R(A) \cap N(A), x \neq 0, \\
\text{则} &\exists y, \text{使得} x = A y, \text{并且} A x = 0. \\
\text{所以}, &0 = A x = A^2 y = A y = x \neq 0 \quad \text{矛盾}. \\
\text{所以}, &R(A) \cap N(A) = \{0\}. \\
\text{有} &\dim R(A) + \dim N(A) = n. \\
\text{所以} &\dim (R(A) + N(A)) = n. \\
\text{因此} \quad &R(A) \oplus N(A) = \mathbf{C}^n.

\end{align*}
$$







