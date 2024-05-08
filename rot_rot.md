<div style="text-align: center; font-size: 40px; font-weight: bold;">
回転を2回とるということについて考える
</div>

</br>

- [なぜそんなことを考えるのか](#なぜそんなことを考えるのか)
- [数式で見てみる](#数式で見てみる)

</br>

## なぜそんなことを考えるのか

</br>

電磁気学ではしばしばマクスウェル方程式から

</br>

$$
\begin{aligned}
\nabla \cdot (\nabla E) + k^2 E &= 0 \newline
\therefore \nabla ^2 E + k^2 E &= 0
\end{aligned}
$$

$\quad ・k:$波数

</br>

を導出する.(ヘルムホルツ方程式)

</br>

右辺の $k$ は波数と呼ばれるもので

$$
k = \frac{2 \pi}{\lambda}
$$

$\quad ・ \lambda:$波長

</br>

の関係がある.これは真空中のスカラー場の電場は上式を満たさなければならないということを意味している.

もし $\lambda$ が定数(これは波長が1つであることを意味している.)だとすると上式の $E$ は $\nabla \cdot \nabla$ という演算の固有関数になっている.つまり

</br>

<div align="center">
<img src="pic\nabla_cdot_nabla.png" alt="alt text" width="300">
</div>

</br>

のように $E$ を入れると $-k^2$ 倍されて出てくる.この演算をスカラーラプラシアンと言う.

</br>

上では電場をスカラー場としたがもし,電場がベクトル場の時は

</br>

$$
\nabla \times (\nabla \times \vec{E}) - k^2 \vec{E} = 0
$$

</br>

となる.(ベクトルヘルムホルツ方程式.)関係する論文は[近軸近似のもとでベクトル場に対するヘルムホルツ方程式を解く](https://github.com/sk0ik/Vector_Beam_Paper_List/blob/main/README.md#%E8%BF%91%E8%BB%B8%E8%BF%91%E4%BC%BC%E3%81%AE%E3%82%82%E3%81%A8%E3%81%A7%E3%83%99%E3%82%AF%E3%83%88%E3%83%AB%E5%A0%B4%E3%81%AB%E5%AF%BE%E3%81%99%E3%82%8B%E3%83%98%E3%83%AB%E3%83%A0%E3%83%9B%E3%83%AB%E3%83%84%E6%96%B9%E7%A8%8B%E5%BC%8F%E3%82%92%E8%A7%A3%E3%81%8F)
を参照.(自分のGithubのページに飛びます.)

</br>

ひとまずこれを受け入れると先ほどのスカラー場の時と同じように

</br>

<div align="center">
<img src="pic\nabla_times_nabla_times.png" alt="alt text" width="300">
</div>

</br>

というような固有関数となるが先ほどと違い, $\vec{E}$ を入れると $k^2 \vec{E}$ のように $k^2$ 倍されて出てくる.この演算をベクトルラプラシアンと言う.

</br>

電場がベクトル場である電磁波(光)はベクトルビームと呼ばれている.これに対応して電場がスカラー場であるものはスカラービームと呼ばれている.例えばスカラービームには直線偏光や円偏光がある.

</br>

まとめると真空中のベクトルビームは回転を2回とるという演算の固有関数になっている.(固有値は $k^2$)

</br>

## 数式で見てみる

</br>

円筒座標系でのナブラは

</br>

$$
\nabla = \vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} + \vec{e} _ z \frac{\partial}{\partial z}
$$

</br>

で表される.スカラー場

</br>

$$
A(r, \theta, z)
$$

</br>

に対してスカラーラプラシアンをとると

</br>

$$
\nabla \cdot (\nabla A) =
\nabla \cdot (\vec{e _ r} \frac{\partial A}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial A}{\partial \theta} + \vec{e} _ z \frac{\partial A}{\partial z})
$$

</br>

$$
(\vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} + \vec{e} _ z \frac{\partial}{\partial z}) \cdot (\vec{e _ r} \frac{\partial A}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial A}{\partial \theta} + \vec{e} _ z \frac{\partial A}{\partial z})
$$

</br>

となるが基底ベクトルの微分

</br>

$$
\frac{\partial}{\partial r} \vec{e} _ r = 0 \frac{\partial}{\partial r} \vec{e} _ \theta = 0\frac{\partial}{\partial r} \vec{e} _ z = 0
$$

</br>

$$
\frac{\partial}{\partial \theta} \vec{e} _ r =
\vec{e} _ \theta, \frac{\partial}{\partial \theta} \vec{e} _ \theta =
-\vec{e} _ r, \frac{\partial}{\partial \theta} \vec{e} _ z =
0
$$

</br>

$$
\frac{\partial}{\partial z} \vec{e} _ r =
0, \frac{\partial}{\partial z} \vec{e} _ \theta =
0, \frac{\partial}{\partial z} \vec{e} _ z =
0
$$

</br>

に気を付けて計算すると

</br>

↓ここから05/05

$$
\vec{e _ r} \frac{\partial}{\partial r} \cdot (\vec{e _ r} \frac{\partial A}{\partial r}) + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} \cdot (\vec{e _ \theta} \frac{1}{r} \frac{\partial A}{\partial \theta}) + \vec{e} _ z \frac{\partial}{\partial z} \cdot (\vec{e} _ z \frac{\partial A}{\partial z})
$$

</br>

$$
= \frac{\partial A}{\partial r} \vec{e _ r} \cdot \frac{\partial \vec{e _ r}}{\partial r} + \frac{\partial ^2 A}{\partial r^2} \vec{e _ r} \cdot \vec{e _ r} + \frac{1}{r^2} \vec{e _ \theta} \cdot \frac{\partial \vec{e _ {\theta}}}{\partial \theta} + \frac{1}{r^2} \frac{\partial ^2 A}{\partial \theta ^2} \vec{e _ \theta} \cdot \vec{e _ {\theta}} + \frac{\partial ^2 A}{\partial z ^2} \vec{e} _ z \cdot \vec{e} _ z + \frac{\partial A}{\partial z} \vec{e} _ z \cdot \frac{\partial \vec{e} _ z}{\partial z}
$$

</br>

$$
= \frac{\partial ^2 A}{\partial r^2} - \frac{1}{r^2} \vec{e _ \theta} \cdot \vec{e _ r} + \frac{1}{r^2} \frac{\partial ^2 A}{\partial \theta ^2} + \frac{\partial ^2 A}{\partial z ^2}
$$

</br>

と外積の線形性を用いて円筒座標系のベクトル場

</br>

$$
\vec{A} = \vec{e} _ r A _ r  + \vec{e} _ {\theta} A _ {\theta} + \vec{e} _ z A _ z
$$

</br>

に対して回転をとると

</br>

$$
\nabla \times \vec{A} =
\Bigl(\vec{e} _ r \frac{\partial}{\partial r}+\frac{1}{r} \vec{e} _ \theta \frac{\partial}{\partial \theta}+\vec{e} _ z \frac{\partial}{\partial z} \Bigr) \times (\vec{e} _ r A _ r+\vec{e} _ {\theta} A _ {\theta} + \vec{e} _ z A _ z)
$$

</br>

$$
= \vec{e} _ r \frac{\partial}{\partial r} \times (\vec{e} _ r A _ r) + \vec{e} _ r \frac{\partial}{\partial r} \times (\vec{e} _ {\theta} A _ {\theta}) + \vec{e} _ r \frac{\partial}{\partial r} \times (\vec{e} _ z A _ z) + \frac{1}{r} \vec{e} _ {\theta} \frac{\partial}{\partial \theta} \times (\vec{e} _ r A _ r) + \frac{1}{r} \vec{e} _ {\theta} \frac{\partial}{\partial \theta} \times (\vec{e} _ {\theta} A _ {\theta}) + \frac{1}{r} \vec{e} _ {\theta} \frac{\partial}{\partial \theta} \times (\vec{e} _ z A _ z) + \vec{e} _ z \frac{\partial}{\partial z} \times (\vec{e} _ r A _ r) + \vec{e} _ z \frac{\partial}{\partial z} \times (\vec{e} _ {\theta} A _ {\theta}) + \vec{e} _ z \frac{\partial}{\partial z} \times (\vec{e} _ {z} A _ {z})
$$

</br>

$$
= A _ r \vec{e} _ r \times \frac{\partial \vec{e} _ r}{\partial r} + \frac{\partial A _ r}{\partial r} \vec{e} _ r \times \vec{e} _ r + A _ {\theta} \vec{e} _ r \times \frac{\partial \vec{e} _ {\theta}}{\partial r} + \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ r \times \vec{e} _ {\theta}
$$

</br>

$$
+A _ z \vec{e} _ r \times \frac{\partial \vec{e} _ z}{\partial r} + \frac{\partial A _ z}{\partial r} \vec{e} _ r \times \vec{e} _ z + \frac{1}{r} A _ r \vec{e} _ {\theta} \times \frac{\partial \vec{e} _ r}{\partial {\theta}} + \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \vec{e} _ {\theta} \times \vec{e} _ r + \frac{1}{r} A _ {\theta} \vec{e} _ {\theta} \times \frac{\partial \vec{e} _ \theta}{\partial \theta}
$$

</br>

$$
+\frac{1}{r} \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ {\theta} \times \vec{e} _ {\theta} + \frac{1}{r} A _ z \vec{e} _ {\theta} \times \frac{\partial \vec{e} _ z}{\partial {\theta}} + \frac{1}{r} \frac{\partial A _ z}{\partial \theta} \vec{e} _ {\theta} \times \vec{e} _ z
$$

</br>

$$
+A _ r \vec{e} _ z \times \frac{\partial \vec{e} _ r}{\partial z}+\frac{\partial A _ r}{\partial z} \vec{e} _ z \times \vec{e} _ r + A _ {\theta} \vec{e} _ z \times \frac{\partial \vec{e} _ {\theta}}{\partial z} + \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ z \times \vec{e} _ {\theta} + A _ z \vec{e} _ z \times \frac{\partial \vec{e} _ z}{\partial z} + \frac{\partial A _ z}{\partial z} \vec{e} _ z \times \vec{e} _ z
$$

</br>

$$
= \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ z - \frac{\partial A _ z}{\partial r} \vec{e} _ {\theta} + \frac{1}{r} A _ r \vec{e} _ {\theta} \times \vec{e} _ {\theta} - \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \vec{e} _ z - \frac{1}{r} A _ {\theta} \vec{e} _ {\theta} \times \vec{e} _ r + \frac{1}{r} \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ {\theta} \times \vec{e} _ {\theta} + \frac{1}{r} \frac{\partial A _ z}{\partial \theta} \vec{e} _ r + \frac{\partial A _ r}{\partial z} \vec{e} _ {\theta} - \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ r
$$

</br>

$$
= \frac{\partial A _ {\theta}}{\partial r} \vec{e} _ z - \frac{\partial A _ z}{\partial r} \vec{e} _ {\theta} - \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \vec{e} _ z + \frac{1}{r} A _ {\theta} \vec{e} _ z + \frac{1}{r} \frac{\partial A _ z}{\partial \theta} \vec{e} _ r + \frac{\partial A _ r}{\partial z} \vec{e} _ {\theta} - \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ r
$$

</br>

$$
= \Bigl(\frac{1}{r} \frac{\partial A _ z}{\partial \theta} - \frac{\partial A _ {\theta}}{\partial z} \vec{e} _ r \Bigr) + \Bigl(\frac{\partial A _ r}{\partial z} - \frac{\partial A _ z}{\partial r} \Bigr)\vec{e} _ {\theta} + \Bigl(\frac{1}{r} A _ {\theta} + \frac{\partial A _ {\theta}}{\partial r} - \frac{1}{r} \frac{\partial A _ r}{\partial \theta} \Bigr)\vec{e} _ z
$$

</br>

を得る.(大変だった.)

</br>

例えば解として2次元極座標で表した

</br>

$$
\vec{A}(r, \theta, z) = re^{-r^2} \vec{e} _ {\theta}
$$

</br>

を仮定する.

</br>

またもう一度回転をとってみると

</br>

$$
\nabla \times (\nabla \times \vec{A}) = -2r^3e^{-r^2} + 8re^{-r^2}
$$

</br>

となるが

</br>

$$
r^3 \ll 1
$$

</br>

であるなら

</br>

$$
\nabla \times (\nabla \times \vec{A}) \propto \vec{A}
$$

</br>

となり

</br>

$$
\nabla \times (\nabla \times)
$$

</br>

という演算の固有関数になっている

雑メモ
- 渦度方程式
- ベクトルポテンシャルの存在（回転とっても０にならない）
