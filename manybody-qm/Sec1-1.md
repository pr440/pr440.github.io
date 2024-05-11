# 同種粒子の不可弁別性
1粒子状態$\left|\psi_i\right\rangle$を持つ粒子が$i=1,2,\ldots,N$まで存在するとき、これら$N$粒子全体の量子状態は、各粒子が識別可能な別種の粒子である場合には、
    \begin{equation}
        \left|\psi\right\rangle\equiv\left|\psi_1\right\rangle\left|\psi_2\right\rangle\cdots\left|\psi_N\right\rangle
    \end{equation}
と通常のテンソル積で表せばよいが、識別不可能な同種粒子である場合にはそのようなテンソル積の状態に粒子を入れ替えてできるテンソル積の状態も等確率で重ね合わせた状態
    \begin{equation}\label{many_body_qsv_def}
        \left|\psi\right\rangle=\left|\psi_1,\psi_2,\cdots,\psi_N\right\rangle\equiv\frac{1}{\sqrt{N!}}\sum_{P}\zeta^P \left|\psi_{P(1)}\right\rangle\left|\psi_{P(2)}\right\rangle\cdots\left|\psi_{P(N)}\right\rangle
    \end{equation}
で表されるべきである。ここで$P$は$\left\\{1,2,\ldots,N\right\\}$に対する置換を表し、総和は可能な全ての置換$P$に対しとっている。同じ粒子の組を2回入れ替えたときには状態が戻るように、$\zeta=\pm 1$に対し、
    \begin{equation}
        \zeta^P=\left\\{
            \begin{array}{cc}
                \zeta & (P\text{が奇置換}) \\
                1 & (P\text{が偶置換}) \\
            \end{array}
        \right.
    \end{equation}
となる。$\zeta=+1$であるような粒子をBose粒子(ボソン)、$\zeta=-1$であるような粒子のことをFermi粒子(フェルミオン)という[^1]。定義から、
    \begin{equation}
        \left|\psi_{P(1)},\psi_{P(2)},\cdots,\psi_{P(N)}\right\rangle=\zeta^{P}\left|\psi_1,\psi_2,\cdots,\psi_N\right\rangle
    \end{equation}
となっており、特にFermi粒子は1粒子状態の並べ方によっては同じ状態の組の多粒子系でも全体の状態の符号が反転しうることに注意する。

Fermi粒子については$N$粒子の中に同じ状態を持つものがあると、その間で入れ替えてできるテンソル積が元のテンソル積と打ち消し合うため、得られる粒子系全体の状態ベクトルが0となってしまう。すなわち、Fermi粒子系では2つ以上の粒子が同じ状態をとることが許されない。これをPauliの排他原理という。

\eqref{many_body_qsv_def}で定義された多体量子状態に対し、同種$N$粒子の量子状態との内積は、
    \begin{align}
        \left\langle \phi\middle|\psi\right\rangle&=\left\langle \phi_1,\phi_2,\cdots,\phi_N\middle|\psi_1,\psi_2,\cdots,\psi_N\right\rangle \\
        &=\frac{1}{N!}\sum_{P,Q}\zeta^P\zeta^{Q} \left\langle\phi_{P(1)}\middle|\psi_{Q(1)}\right\rangle\left\langle\phi_{P(2)}\middle|\psi_{Q(2)}\right\rangle\cdots\left\langle\phi_{P(N)}\middle|\psi_{Q(N)}\right\rangle \\
        &=\sum_{R}\zeta^R \left\langle\phi_1\middle|\psi_{R(1)}\right\rangle\left\langle\phi_2\middle|\psi_{R(2)}\right\rangle\cdots\left\langle\phi_N\middle|\psi_{R(N)}\right\rangle
    \end{align}
で与えられる。ここで、$P,Q,R$は$\left\\{1,2,\ldots,N\right\\}$に対する置換を表し、$R=P^{-1}\circ Q$である。総和は全て可能な置換$P,Q,R$に対しとっている。特に、$\zeta=-1$のFermi粒子系の場合、この内積は、
    \begin{equation}
        \left\langle \phi\middle|\psi\right\rangle=
            \begin{vmatrix}
                \left\langle\phi_1\middle|\psi_1\right\rangle & \left\langle\phi_1\middle|\psi_2\right\rangle & \cdots & \left\langle\phi_1\middle|\psi_N\right\rangle \\
                \left\langle\phi_2\middle|\psi_1\right\rangle & \left\langle\phi_2\middle|\psi_2\right\rangle & \cdots & \left\langle\phi_2\middle|\psi_N\right\rangle \\
                \vdots & \vdots & \ddots & \vdots \\
                \left\langle\phi_N\middle|\psi_1\right\rangle & \left\langle\phi_N\middle|\psi_2\right\rangle & \cdots & \left\langle\phi_N\middle|\psi_N\right\rangle \\
            \end{vmatrix}
    \end{equation}
というように行列式で表される。また、同様にしてケット-ブラの積も
    \begin{equation}
        \left|\phi\right\rangle\!\left\langle\psi\right|=\sum_{P}\zeta^P \left(\left|\phi_1\right\rangle\!\left\langle\psi_{P(1)}\right|\right)\otimes\left(\left|  \phi_2\right\rangle\!\left\langle\psi_{P(2)}\right|\right)\otimes\cdots\otimes\left(\left|\phi_N\right\rangle\!\left\langle\psi_{P(N)}\right|\right)
    \end{equation}
で与えられることがわかる。

正規直交系をなす1粒子状態の正規直交系$\left\\{\left|\alpha_i\right\rangle\right\\}$を用意すると、
    \begin{align}
        &\frac{1}{N!}\sum_{i_1,i_2,\cdots,i_N}\left|\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right\rangle\!\left\langle\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right|\\
        &\qquad=\frac{1}{N!}\sum_{i_1,i_2,\cdots,i_N}\sum_{P}\zeta^P \left(\left|\alpha_{i_1}\right\rangle\!\left\langle\alpha_{i_{P(1)}}\right|\right)\otimes\left(\left|\alpha_{i_2}\right\rangle\!\left\langle\alpha_{i_{P(2)}}\right|\right)\otimes\cdots\otimes\left(\left|\alpha_{i_N}\right\rangle\!\left\langle\alpha_{i_{P(N)}}\right|\right) \\
        &\qquad=\frac{1}{N!}\sum_{i_1,i_2,\cdots,i_N}\sum_{P}\zeta^P \left(\left|\alpha_{i_{P(1)}}\right\rangle\!\left\langle\alpha_{i_1}\right|\right)\otimes\left(\left|\alpha_{i_{P(2)}}\right\rangle\!\left\langle\alpha_{i_2}\right|\right)\otimes\cdots\otimes\left(\left|\alpha_{i_{P(N)}}\right\rangle\!\left\langle\alpha_{i_N}\right|\right)
    \end{align}
に対して、$\left|\alpha_{j_1},\alpha_{j_2},\cdots,\alpha_{j_N}\right\rangle$を右から作用させると、
    \begin{align}
        &\left[\frac{1}{N!}\sum_{i_1,i_2,\cdots,i_N}\sum_{P}\zeta^P \left(\left|\alpha_{i_{P(1)}}\right\rangle\!\left\langle\alpha_{i_1}\right|\right)\otimes\left(\left|\alpha_{i_{P(2)}}\right\rangle\!\left\langle\alpha_{i_2}\right|\right)\otimes\cdots\otimes\left(\left|\alpha_{i_P(N)}\right\rangle\!\left\langle\alpha_{i_N}\right|\right)\right]\left|\alpha_{j_1},\alpha_{j_2},\cdots,\alpha_{j_N}\right\rangle \\
        &\qquad =\left(\frac{1}{N!}\right)^{3/2}\sum_{i_1,i_2,\cdots,i_N}\sum_{P,Q}\zeta^P\zeta^Q \left|\alpha_{i_{P(1)}}\right\rangle\left|\alpha_{i_{P(2)}}\right\rangle\cdots\left|\alpha_{i_P(N)}\right\rangle\left\langle\alpha_{i_1}\middle|\alpha_{j_{Q(1)}}\right\rangle\left\langle\alpha_{i_2}\middle|\alpha_{j_{Q(2)}}\right\rangle\cdots\left\langle\alpha_{i_N}\middle|\alpha_{j_{Q(N)}}\right\rangle \\
        &\qquad =\left(\frac{1}{N!}\right)^{3/2}\sum_{P,Q}\zeta^P\zeta^Q \left|\alpha_{j_{Q\circ P(1)}}\right\rangle\left|\alpha_{j_{Q\circ P(2)}}\right\rangle\cdots\left|\alpha_{j_{Q\circ P(N)}}\right\rangle \\
        &\qquad =\frac{1}{\sqrt{N!}}\sum_{R}\zeta^R \left|\alpha_{j_{R(1)}}\right\rangle\left|\alpha_{j_{R(2)}}\right\rangle\cdots\left|\alpha_{j_{R(N)}}\right\rangle=\left|\alpha_{j_1},\alpha_{j_2},\cdots,\alpha_{j_N}\right\rangle
    \end{align}
となることから、完全性関係
    \begin{equation}\label{complete-relation_N-particle}
        \frac{1}{N!}\sum_{i_1,i_2,\cdots,i_N}\left|\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right\rangle\!\left\langle\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right|=\hat{I}^{(N)}
    \end{equation}
が導かれる($\hat{I}^{(N)}$は$N$粒子状態に対する恒等演算子)。$\left\\{\left|\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right\rangle\right\\}$は、Fermi粒子の場合には$i_1<i_2<\cdots <i_N$の条件[^2]のもとで正規直交系をなす一方、Bose粒子の場合には$i_1\leq i_2\leq \cdots \leq i_N$の条件を課しても直交系は成すが正規化は満たされない。実際に、1粒子状態$\left|\alpha_i\right\rangle$を持つ粒子が$n_i$個ある$N$粒子系の状態のノルムは
    \begin{equation}
        \left\langle\alpha_1,\cdots,\alpha_1,\alpha_2,\cdots\middle|\alpha_1,\cdots,\alpha_1,\alpha_2\cdots\right\rangle=\prod_i (n_i)!
    \end{equation}
となることが導かれる。

以上で議論してきた$N$粒子状態を$N=0$の場合でも考えておくと、粒子がないという状態は(位相の不定性を除いて)1つしかない。それを$\left|0\right\rangle$とおき($\left\langle 0\middle| 0\right\rangle=1$とする)、真空状態と呼ぶ。

1粒子系の量子力学において状態はHilbert空間$\mathfrak{H}$の元であった[^3]。それに対して、N粒子系の状態は1粒子状態のHilbert空間のテンソル積$\mathfrak{H}^{\otimes N}$の元となる。多体系の量子状態はそれの$N$に対する直和の元となるが、この空間はFock空間と呼ばれる。

[^1]: 上の$\zeta^P$の定義は$\zeta=\pm 1$のときのみである。$\left|\zeta\right|=1$を満たす範囲で$\zeta$は複素数に拡張すると、$\zeta^P$は置換$P$を互換の積に直したときの積の個数だけ$\zeta$の冪乗をとることで与えられる。$\zeta\neq\pm 1$であるような粒子はエニオンと呼ばれる。

[^2]: ある1粒子状態の組で表される多体状態が一意に定まるように状態のとり方を制限している。Bose粒子での条件も同じ。

[^3]: 「1粒子状態の完全系」は$\mathfrak{H}$を張る状態の集合の意味で用いている。以降も同様。