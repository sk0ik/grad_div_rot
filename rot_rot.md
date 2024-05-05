# 回転を2回とるということについて考える

1. [回転を2回とるということについて考える](#回転を2回とるということについて考える)
   1. [なぜそんなことを考えるのか](#なぜそんなことを考えるのか)
   2. [数式で見てみる](#数式で見てみる)
2. [\\frac{\\partial}{\\partial r} \\vec{e} \_ r](#fracpartialpartial-r-vece-_-r)
3. [0,\\frac{\\partial}{\\partial r} \\vec{e} \_ \\theta](#0fracpartialpartial-r-vece-_-theta)
4. [0,\\frac{\\partial}{\\partial r} \\vec{e} \_ z](#0fracpartialpartial-r-vece-_-z)
5. [\\frac{\\partial}{\\partial \\theta} \\vec{e} \_ r](#fracpartialpartial-theta-vece-_-r)
6. [\\vec{e} \_ \\theta, \\frac{\\partial}{\\partial \\theta} \\vec{e} \_ \\theta](#vece-_-theta-fracpartialpartial-theta-vece-_-theta)
7. [-\\vec{e} \_ r, \\frac{\\partial}{\\partial \\theta} \\vec{e} \_ z](#-vece-_-r-fracpartialpartial-theta-vece-_-z)
8. [\\frac{\\partial}{\\partial z} \\vec{e} \_ r](#fracpartialpartial-z-vece-_-r)
9. [0, \\frac{\\partial}{\\partial z} \\vec{e} \_ \\theta](#0-fracpartialpartial-z-vece-_-theta)
10. [0, \\frac{\\partial}{\\partial z} \\vec{e} \_ z](#0-fracpartialpartial-z-vece-_-z)

## なぜそんなことを考えるのか

電磁気学ではしばしばマクスウェル方程式から

$$
\begin{aligned}
\nabla \cdot (\nabla E) + k^2 E &= 0 \newline
\therefore \nabla ^2 E + k^2 E &= 0
\end{aligned}
$$

- $k:$波数

を導出する.(ヘルムホルツ方程式)

右辺の $k$ は波数と呼ばれるもので

$$
k = \frac{2 \pi}{\lambda}
$$

- $\lambda:$波長

の関係がある.これは真空中のスカラー場の電場は上式を満たさなければならないということを意味している.

もし $\lambda$ が定数(これは波長が1つであることを意味している.)だとすると上式の $E$ は $\nabla \cdot \nabla$ という演算の固有関数になっている.つまり

<div align="center">
<img src="pic\nabla_cdot_nabla.png" alt="alt text" width="300">
</div>

のように $E$ を入れると $-k^2$ 倍されて出てくる.この演算をスカラーラプラシアンと言う.

上では電場をスカラー場としたがもし,電場がベクトル場の時は

$$
\nabla \times (\nabla \times \vec{E}) - k^2 \vec{E} = 0
$$

となる.(ベクトルヘルムホルツ方程式.)関係する論文は[近軸近似のもとでベクトル場に対するヘルムホルツ方程式を解く](https://github.com/sk0ik/Vector_Beam_Paper_List/blob/main/README.md#%E8%BF%91%E8%BB%B8%E8%BF%91%E4%BC%BC%E3%81%AE%E3%82%82%E3%81%A8%E3%81%A7%E3%83%99%E3%82%AF%E3%83%88%E3%83%AB%E5%A0%B4%E3%81%AB%E5%AF%BE%E3%81%99%E3%82%8B%E3%83%98%E3%83%AB%E3%83%A0%E3%83%9B%E3%83%AB%E3%83%84%E6%96%B9%E7%A8%8B%E5%BC%8F%E3%82%92%E8%A7%A3%E3%81%8F)
を参照.(自分のGithubのページに飛びます.)

ひとまずこれを受け入れると先ほどのスカラー場の時と同じように

<div align="center">
<img src="pic\nabla_times_nabla_times.png" alt="alt text" width="300">
</div>

というような固有関数となるが先ほどと違い, $\vec{E}$ を入れると $k^2 \vec{E}$ のように $k^2$ 倍されて出てくる.この演算をベクトルラプラシアンと言う.

電場がベクトル場である電磁波(光)はベクトルビームと呼ばれている.これに対応して電場がスカラー場であるものはスカラービームと呼ばれている.例えばスカラービームには直線偏光や円偏光がある.

まとめると真空中のベクトルビームは回転を2回とるという演算の固有関数になっている.(固有値は $k^2$)

## 数式で見てみる

円筒座標系でのナブラは

$$
\nabla = \vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} + \vec{e} _ z \frac{\partial}{\partial z}
$$

で表される.スカラー場

$$
A(r, \theta, z)
$$

に対してスカラーラプラシアンをとると

$$
\nabla \cdot (\nabla A) =
\nabla \cdot (\vec{e _ r} \frac{\partial A}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial A}{\partial \theta} + \vec{e} _ z \frac{\partial A}{\partial z})
$$

$$
(\vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} + \vec{e} _ z \frac{\partial}{\partial z}) \cdot (\vec{e _ r} \frac{\partial A}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial A}{\partial \theta} + \vec{e} _ z \frac{\partial A}{\partial z})
$$

となるが基底ベクトルの微分

$$
\frac{\partial}{\partial r} \vec{e} _ r
=
0,\frac{\partial}{\partial r} \vec{e} _ \theta
=
0,\frac{\partial}{\partial r} \vec{e} _ z
=
0
$$

$$
\frac{\partial}{\partial \theta} \vec{e} _ r
=
\vec{e} _ \theta, \frac{\partial}{\partial \theta} \vec{e} _ \theta
=
-\vec{e} _ r, \frac{\partial}{\partial \theta} \vec{e} _ z
=
0
$$

$$
\frac{\partial}{\partial z} \vec{e} _ r
=
0, \frac{\partial}{\partial z} \vec{e} _ \theta
=
0, \frac{\partial}{\partial z} \vec{e} _ z
=
0
$$

に気を付けて計算すると

↓ここから05/05

$$
\vec{e _ r} \frac{\partial}{\partial r} \cdot (\vec{e _ r} \frac{\partial A}{\partial r}) + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} \cdot (\vec{e _ \theta} \frac{1}{r} \frac{\partial A}{\partial \theta}) + \vec{e} _ z \frac{\partial}{\partial z} \cdot (\vec{e} _ z \frac{\partial A}{\partial z})
$$

$$
= \frac{\partial A}{\partial r} \vec{e _ r} \cdot \frac{\partial \vec{e _ r}}{\partial r} + \frac{\partial ^2 A}{\partial r^2} \vec{e _ r} \cdot \vec{e _ r} + \frac{1}{r^2} \vec{e _ \theta} \cdot \frac{\partial \vec{e _ {\theta}}}{\partial \theta} + \frac{1}{r^2} \frac{\partial ^2 A}{\partial \theta ^2} \vec{e _ \theta} \cdot \vec{e _ {\theta}} + \frac{\partial ^2 A}{\partial z ^2} \vec{e} _ z \cdot \vec{e} _ z + \frac{\partial A}{\partial z} \vec{e} _ z \cdot \frac{\partial \vec{e} _ z}{\partial z}
$$

$$
= \frac{\partial ^2 A}{\partial r^2} - \frac{1}{r^2} \vec{e _ \theta} \cdot \vec{e _ r} + \frac{1}{r^2} \frac{\partial ^2 A}{\partial \theta ^2} + \frac{\partial ^2 A}{\partial z ^2}
$$

と外積の線形性を用いて円筒座標系のベクトル場

$$
\vec{A} = \vec{e} _ r A _ r  + \vec{e} _ {\theta} A _ {\theta} + \vec{e} _ z A _ z
$$

に対して回転をとると

$$
\nabla \times \vec{A} =
\Bigl(\vec{e} _ r \frac{\partial}{\partial r}+\frac{1}{r} \vec{e} _ \theta \frac{\partial}{\partial \theta}+\vec{e} _ z \frac{\partial}{\partial z} \Bigr) \times (\vec{e} _ r A _ r+\vec{e} _ {\theta} A _ {\theta} + \vec{e} _ z A _ z)
$$

$$
= \vec{e} _ r \frac{\partial}{\partial r} \times (\vec{e} _ r A _ r) + \vec{e} _ r \frac{\partial}{\partial r} \times (\vec{e} _ {\theta} A _ {\theta}) + \vec{e} _ r \frac{\partial}{\partial r} \times (\vec{e} _ z A _ z) + \frac{1}{r} \vec{e} _ {\theta} \frac{\partial}{\partial \theta} \times (\vec{e} _ r A _ r) + \frac{1}{r} \vec{e} _ {\theta} \frac{\partial}{\partial \theta} \times (\vec{e} _ {\theta} A _ {\theta}) + \frac{1}{r} \vec{e} _ {\theta} \frac{\partial}{\partial \theta} \times (\vec{e} _ z A _ z) + \vec{e} _ z \frac{\partial}{\partial z} \times (\vec{e} _ r A _ r) + \vec{e} _ z \frac{\partial}{\partial z} \times (\vec{e} _ {\theta} A _ {\theta}) + \vec{e} _ z \frac{\partial}{\partial z} \times (\vec{e} _ {z} A _ {z})
$$

$$
= A _ r \vec{e} _ r \times \frac{\partial \vec{e} _ r}{\partial r} + \frac{\partial A _ r}{\partial r} \vec{e} _ r \times \vec{e} _ r + A _ {\theta} \vec{e} _ r \times \frac{\partial \vec{e} _ {\theta}}{\partial r} + \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ r \times \vec{e} _ {\theta}  + A _ z \vec{e} _ r \times \frac{\partial \vec{e} _ z}{\partial r} + \frac{\partial A _ z}{\partial r} \vec{e} _ r \times \vec{e} _ z + \frac{1}{r} A _ r \vec{e} _ {\theta} \times \frac{\partial \vec{e} _ r}{\partial {\theta}} + \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \vec{e} _ {\theta} \times \vec{e} _ r + \frac{1}{r} A _ {\theta} \vec{e} _ {\theta} \times \frac{\partial \vec{e} _ \theta}{\partial \theta} + \frac{1}{r} \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ {\theta} \times \vec{e} _ {\theta} + \frac{1}{r} A _ z \vec{e} _ {\theta} \times \frac{\partial \vec{e} _ z}{\partial {\theta}} + \frac{1}{r} \frac{\partial A _ z}{\partial \theta} \vec{e} _ {\theta} \times \vec{e} _ z + A _ r \vec{e} _ z \times \frac{\partial \vec{e} _ r}{\partial z}+\frac{\partial A _ r}{\partial z} \vec{e} _ z \times \vec{e} _ r + A _ {\theta} \vec{e} _ z \times \frac{\partial \vec{e} _ {\theta}}{\partial z} + \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ z \times \vec{e} _ {\theta} + A _ z \vec{e} _ z \times \frac{\partial \vec{e} _ z}{\partial z} + \frac{\partial A _ z}{\partial z} \vec{e} _ z \times \vec{e} _ z
$$

$$
= \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ z - \frac{\partial A _ z}{\partial r} \vec{e} _ {\theta} + \frac{1}{r} A _ r \vec{e} _ {\theta} \times \vec{e} _ {\theta} - \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \vec{e} _ z - \frac{1}{r} A _ {\theta} \vec{e} _ {\theta} \times \vec{e} _ r + \frac{1}{r} \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ {\theta} \times \vec{e} _ {\theta} + \frac{1}{r} \frac{\partial A _ z}{\partial \theta} \vec{e} _ r + \frac{\partial A _ r}{\partial z} \vec{e} _ {\theta} - \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ r
$$

$$
= \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ z - \frac{\partial A _ z}{\partial r} \vec{e} _ {\theta} - \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \vec{e} _ z + \frac{1}{r} A _ {\theta} \vec{e} _ z + \frac{1}{r} \frac{\partial A _ z}{\partial \theta} \vec{e} _ r + \frac{\partial A _ r}{\partial z} \vec{e} _ {\theta} - \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ r
$$

$$
= \Bigl(\frac{1}{r} \frac{\partial A _ z}{\partial \theta} - \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ r \Bigr) + \Bigl(\frac{\partial A _ r}{\partial z} - \frac{\partial A _ z}{\partial r} \Bigr)\vec{e} _ {\theta} + \Bigl(\frac{1}{r} A _ {\theta} + \frac{\partial A _ {\theta}}{\partial r} - \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \Bigr)\vec{e} _ z
$$

を得る.(大変だった.)

例えば解として2次元極座標で表した

$$
\vec{A}(r, \theta, z) = re^{-r^2} \vec{e} _ {\theta}
$$

を仮定する.

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

雑メモ
- 渦度方程式
- ベクトルポテンシャルの存在（回転とっても０にならない）
