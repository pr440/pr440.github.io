# 1.2 生成消滅演算子
$N$粒子系の量子状態$\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle$と、それに1粒子状態$\left\lvert\phi\right\rangle$の粒子を加え入れた$(N+1)$粒子系の量子状態$\left\lvert\psi_1,\psi_2,\cdots,\psi_N,\phi\right\rangle$に対し、次のような作用をもつ演算子$\hat{a}^{\dagger}(\phi)$を考える。
	\begin{equation}
		\hat{a}^\dagger(\phi)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle=\left\lvert\phi,\psi_1,\psi_2,\cdots,\psi_N\right\rangle
	\end{equation}
$(N+1)$粒子系の量子状態$\left\lvert\chi_1,\chi_2,\cdots,\chi_{N+1}\right\rangle$と上式の両辺との内積をとり、複素共役をとると、
	\begin{align}
		&\left\langle\psi_1,\psi_2,\cdots,\psi_N\right\rvert\!\hat{a}(\phi)\!\left\lvert\chi_1,\chi_2,\cdots,\chi_{N+1}\right\rangle=\left\langle\phi,\psi_1,\psi_2,\cdots,\psi_N\middle\vert\chi_1,\chi_2,\cdots,\chi_{N+1}\right\rangle \\\\\\
		&\qquad =\sum_{P}\zeta^P \left\langle\phi\middle\vert\chi_{P(1)}\right\rangle\left\langle\psi_1\middle\vert\chi_{P(2)}\right\rangle\left\langle\psi_2\middle\vert\chi_{P(3)}\right\rangle\cdots\left\langle\psi_N\middle\vert\chi_{P(N+1)}\right\rangle \\\\\\
		&\qquad =\sum_{k}\zeta^{k-1}\left\langle\phi\middle\vert\chi_k\right\rangle\sum_{Q}\zeta^Q \left\langle\psi_1\middle\vert\chi_{Q(1)}\right\rangle\left\langle\psi_2\middle\vert\chi_{Q(2)}\right\rangle\cdots\left\langle\psi_N\middle\vert\chi_{Q(N)}\right\rangle \\\\\\
		&\qquad =\sum_{k}\zeta^{k-1}\left\langle\phi\middle\vert\chi_k\right\rangle\left\langle\psi_1,\psi_2,\cdots,\psi_N\middle\vert\chi_1,\chi_2,\cdots\chi_{k-1},\chi_{k+1}\cdots,\chi_{N+1}\right\rangle
	\end{align}
となる($P$は$\left\\{1,2,\hdots,N\right\\}$の置換、$Q$は$\left\\{1,2\hdots,k-1,k+1,\hdots,N\right\\}$の置換)ことから、$\hat{a}(\phi)$の作用が
	\begin{equation}
		\hat{a}(\phi)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle=\sum_{k}\zeta^{k-1}\left\langle\phi\middle\vert\chi_k\right\rangle\left\lvert\psi_1,\psi_2,\cdots\psi_{k-1},\chi_{k+1}\cdots,\psi_{N}\right\rangle
	\end{equation}
と表せることがわかる。ここで右辺は全ての$\left\lvert\chi_i\right\rangle$で$\left\langle\phi\middle\vert\chi_i\right\rangle=0$である場合は0に、それ以外の場合は$(N-1)$粒子系の量子状態になっていることに注意する。
		
このようにして系に粒子を追加・減少させる演算子$\hat{a}^\dagger(\phi),\hat{a}(\phi)$を構成できた。これらの演算子を生成消滅演算子という。
	\begin{align}
		\hat{a}(\phi_1)\hat{a}^\dagger(\phi_2)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle&=\left\langle\phi_1\middle\vert\phi_2\right\rangle\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle \\\\\\ &\qquad +\sum_{k}\zeta^{k}\left\langle\phi_1\middle\vert\chi_k\right\rangle\left\lvert\phi_2,\psi_1,\psi_2,\cdots\psi_{k-1},\chi_{k+1}\cdots,\psi_{N}\right\rangle\\\\\\
		\hat{a}^\dagger(\phi_2)\hat{a}(\phi_1)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle&=\sum_{k}\zeta^{k-1}\left\langle\phi_1\middle\vert\chi_k\right\rangle\left\lvert\psi_1,\psi_2,\cdots\psi_{k-1},\chi_{k+1}\cdots,\psi_{N},\phi_2\right\rangle
	\end{align}
となることから、
	\begin{equation}	\label{commutation_relation}
		\left[\hat{a}(\phi_1),\hat{a}^\dagger(\phi_2)\right]_{-\zeta}\equiv\hat{a}(\phi_1)\hat{a}^\dagger(\phi_2)-\zeta\hat{a}^\dagger(\phi_2)\hat{a}(\phi_1)=\left\langle\phi_1\middle\vert\phi_2\right\rangle
	\end{equation}
が成り立つことがわかる。$[\hat{A},\hat{B}]_{-\zeta}$は$\zeta=+1$のBose粒子のときには交換子$[\hat{A},\hat{B}]$、$\zeta=-1$のFermi粒子のときは反交換子$\\{\hat{A},\hat{B}\\}$である。生成演算子同士、消滅演算子同士の交換・反交換子は、
	\begin{align}
		\hat{a}^\dagger(\phi_1)\hat{a}^\dagger(\phi_2)\left\lvert\phi_1,\phi_2,\psi_1,\psi_2,\cdots,\psi_N\right\rangle&=\left\lvert\psi_1,\psi_2,\cdots\psi_{k-1},\chi_{k+1}\cdots,\psi_{N}\right\rangle \\\\\\
		&=\zeta\left\lvert\phi_2,\phi_1\psi_1,\psi_2,\cdots\psi_{k-1},\chi_{k+1}\cdots,\psi_{N}\right\rangle \\\\\\
		&=\zeta\hat{a}^\dagger(\phi_2)\hat{a}^\dagger(\phi_1)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle 
	\end{align}
	\begin{align}
		\hat{a}(\phi_1)\hat{a}(\phi_2)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle&=\sum_{k<l}\zeta^{k-1}\zeta^{l-1}\left\langle\phi_1\middle\vert\chi_k\right\rangle\left\langle\phi_2\middle\vert\chi_l\right\rangle\left\lvert\psi_1,\psi_2,\cdots(\psi_{k},\psi_{l}\text{のみなし})\cdots,\psi_{N}\right\rangle \\\\\\
		&\qquad +\sum_{k>l}\zeta^{k-2}\zeta^{l-1}\left\langle\phi_1\middle\vert\chi_k\right\rangle\left\langle\phi_2\middle\vert\chi_l\right\rangle\left\lvert\psi_1,\psi_2,\cdots(\psi_{k},\psi_{l}\text{のみなし})\cdots,\psi_{N}\right\rangle \\\\\\
		&=\zeta\sum_{k>l}\zeta^{k-1}\zeta^{l-1}\left\langle\phi_2\middle\vert\chi_l\right\rangle\left\langle\phi_1\middle\vert\chi_k\right\rangle\left\lvert\psi_1,\psi_2,\cdots(\psi_{k},\psi_{l}\text{のみなし})\cdots,\psi_{N}\right\rangle \\\\\\
		&\qquad +\zeta\sum_{k<l}\zeta^{k-2}\zeta^{l-1}\left\langle\phi_2\middle\vert\chi_l\right\rangle\left\langle\phi_1\middle\vert\chi_k\right\rangle\left\lvert\psi_1,\psi_2,\cdots(\psi_{k},\psi_{l}\text{のみなし})\cdots,\psi_{N}\right\rangle \\\\\\
		&=\zeta\hat{a}(\phi_1)\hat{a}(\phi_2)\left\lvert\psi_1,\psi_2,\cdots,\psi_N\right\rangle
	\end{align}
なので、
	\begin{equation}
		\left[\hat{a}(\phi_1),\hat{a}(\phi_2)\right]_{-\zeta}=0,\quad \left[\hat{a}^\dagger(\phi_1),\hat{a}^\dagger(\phi_2)\right]_{-\zeta}=0
	\end{equation}
となる[^1]。

前節の正規直交系をなす1粒子状態の完全系$\left\\{\left\lvert\alpha_i\right\rangle\right\\}$を再び用いる。$\hat{a}(\alpha_i)=\hat{a}_i$と表すことにすると、
	\begin{align}
		\hat{a}^\dagger_i\hat{a}_i\left\lvert\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right\rangle&=\sum_{k}\zeta^{k-1}\left\langle\alpha_i\middle\vert\alpha_{i_k}\right\rangle\left\lvert\alpha_i,\alpha_{i_1},\alpha_{i_2},\cdots\alpha_{i_{k-1}},\alpha_{i_{k+1}}\cdots,\alpha_{i_N}\right\rangle \\\\\\
		&=\sum_{k}\left\langle\alpha_i\middle\vert\alpha_{i_k}\right\rangle\left\lvert\alpha_{i_1},\alpha_{i_2},\cdots\alpha_{i_{k-1}},\alpha_i,\alpha_{i_{k+1}}\cdots,\alpha_{i_N}\right\rangle \\\\\\
		&=n_i\left\lvert\alpha_{i_1},\alpha_{i_2},\cdots\alpha_{i_{k-1}},\alpha_{i_k}\alpha_{i_{k+1}}\cdots,\alpha_{i_N}\right\rangle
	\end{align}
となり、$\hat{n}_i\equiv\hat{a}^\dagger_i\hat{a}$に対して$\left\lvert\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right\rangle$は固有値$n_i$の固有状態となることがわかる。また、$n_i$は$\left\lvert\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_N}\right\rangle$に含まれる1粒子状態$\left\lvert\alpha_i\right\rangle$の粒子数である。すなわち、$\hat{n}_i$の固有値はBose粒子系では$n_i=0,1,2,\hdots$に、Fermi粒子系では$n_i=0,1$に限られる。1粒子状態の直交系に対応した$\hat{n}_i$の組があれば、
	\begin{equation}
		\hat{N}=\sum_i\hat{n}_i
	\end{equation}
は系の総粒子数を与える演算子になることもわかる。

生成消滅演算子の導入により、異なる粒子数状態の間での内積が必ず0になることが示される。なぜなら、任意の多粒子系に量子状態は存在する粒子の1粒子状態の数だけ生成演算子を真空に作用させることで得られるため、粒子数の違う状態間での内積は生成演算子と消滅演算子の数がつりあわず、交換関係・反交換関係を用いることで消滅演算子が真空ケットベクトルに、あるいは生成演算子が真空ブラベクトルに作用するように変形することができて、そのような項は0になるからである。また、$N$粒子状態空間上での完全性関係が\eqref{complete-relation_N-particle}で与えられたことから、Fock空間全体での恒等演算子$\hat{I}$を与える完全性関係が
	\begin{align}
		\hat{I}&=\sum_{N=0}^\infty\frac{1}{N!}\sum_{i_1,i_2,\hdots,i_N}\hat{a}_{i_1}^\dagger\hat{a}_{i_2}^\dagger\cdots\hat{a}_{i_N}^\dagger\hat{a}_{i_N}\cdots\hat{a}_{i_2}\hat{a}_{i_1}
	\end{align}
で与えられることもわかる。

[^1]: ここで、前節で見たFermi粒子系の多粒子状態が1粒子状態の並べ方で符号を反転させうることを再考すると、Fermi粒子系は生成演算子の並べ方についての情報を状態の符号という形で有していることがわかる。