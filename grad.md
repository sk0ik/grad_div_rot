# 勾配

$$
\nabla \cdot (\nabla A) = -k A
$$

$$
\nabla = \vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta}
$$

$z=0$ でのガウシアンビーム

$$
E = e^{-r^2}
$$

に対して

$$
\nabla \cdot (\nabla E)
$$

を考える.

まず勾配

$$
\begin{aligned}
\nabla E
&=
\vec{e _ r} \frac{\partial E}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial E}{\partial \theta} \newline
&=
 \vec{e _ r} \frac{\partial e^{-r^2}}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial e^{-r^2}}{\partial \theta} \newline
 \therefore \nabla E
 &=
 \vec{e _ r} (-2re^{-r^2})
\end{aligned}
$$

そして発散

$$
\begin{aligned}
\nabla \cdot (\nabla E)
&=
\nabla \cdot \{\vec{e _ r(-2re^{-r^2})}\} \newline
&=
\Bigl(\vec{e _ r} \frac{\partial}{\partial r} + \vec{e _ \theta} \frac{1}{r} \frac{\partial}{\partial \theta} \Bigr) \cdot \{{\vec{e} _ r(-2re^{-r^2})}\} \newline
&=
\frac{\partial}{\partial r} (-2re^{-r^2}) \newline
&=
-2 \frac{\partial}{\partial r} (re^{-r^2}) \newline
&=
-2(1 -2r^2) e^{-r^2} \newline
&=
4 r^2 e^{-r^2} - 2 e^{-r^2} \newline
& \approx
-2 e^{-r^2} \newline
& \propto e^{-r^2} \newline
\therefore \nabla \cdot (\nabla E)
& \propto
e^{-r^2} \quad (r^2 \ll 1)
\end{aligned}
$$