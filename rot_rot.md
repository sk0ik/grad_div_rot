突然だが以下のような方程式を考える.

$$
\nabla \times (\nabla \times \vec{E}) = k \vec{E}
$$

- $k:$波数

右辺の $k$ は波数と呼ばれるもので

$$
k = \frac{2 \pi}{\lambda}
$$

で表される.もし $\lambda$ が定数(これは波長が1つであることを意味している.)だとすると上式の $\vec{E}$ は $\nabla \times \nabla \times$ という演算の固有関数になっている.つまり

<div align="center">
<img src="pic\nabla_times_nabla_times.png" alt="alt text" width="300">
</div>

のように $\vec{E}$ を入れると $k \vec{E}$ のように $k$ 倍されて出てくる.

そこで解として

$$
\vec{A} = re^{-r^2} \vec{e} _ r
$$

を仮定する.２次元極座標でのナブラは

$$
\nabla = \vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta}
$$

でるので基底ベクトルの微分

$$
\begin{aligned}
\frac{\partial}{\partial \theta} \vec{e} _ \theta
&=
-\vec{e} _ r \newline
\frac{\partial}{\partial r} \vec{e} _ r
&=
0 \newline
\frac{\partial}{\partial r} \vec{e} _ \theta
&=
0 \newline
\frac{\partial}{\partial \theta} \vec{e} _ r
&=
\vec{e} _ \theta
\end{aligned}
$$

に注意して回転をとると

$$
\begin{aligned}
\nabla \times \vec{A}
&=
\Bigl(\vec{e} _ r \frac{\partial}{\partial r} + \vec{e} _ \theta \frac{1}{r} \frac{\partial}{\partial \theta}\Bigr
) \times \vec{e} _ r r e^{-r^2}
\newline
&=

\end{aligned}
$$

またもう一度回転をとってみると

$$
\nabla \times (\nabla \times \vec{A}) = -2r^3e^{-r^2} + 8re^{-r^2}
$$

となるが

$$
r^3 \ll 1
$$

であるなら

$$
\nabla \times (\nabla \times \vec{A}) \propto \vec{A}
$$

となり

$$
\nabla \times (\nabla \times)
$$

という演算の固有関数になっている

メモ
- 渦度方程式
- ベクトルポテンシャルの存在（回転とっても０にならない）