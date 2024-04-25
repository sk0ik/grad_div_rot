# 回転

$$
\nabla = \frac{\partial}{\partial x} \vec{e _ x} + 
\frac{\partial}{\partial y} \vec{e _ y} +
\frac{\partial}{\partial z} \vec{e _ z}
$$

をベクトル場 $\vec{A}$ に対して

$$
\nabla \times \vec{A}
$$

を回転をとる,と言う.具体的には

$$
\nabla \times \vec{A} = 
\bigl(\frac{\partial A _ z}{\partial y} - \frac{\partial A _ y }{\partial z}\bigr) \vec{e _ x} + 
\bigl(\frac{\partial A _ x}{\partial z} - \frac{\partial A _ z } {\partial x}\bigr) \vec{e _ y} + 
\bigl(\frac{\partial A _ y}{\partial x} - \frac{\partial A _ x}{\partial y} \bigr) \vec{e _ z}
$$

と書ける.

円筒極座標では

$$
\nabla \times \vec{A} = \biggl(\frac{1}{r} \frac{\partial A _ z}{\partial \theta} - \frac{\partial A _ \theta}{\partial z} \biggr)\vec{e _ r} + \biggl(\frac{\partial A _ r}{\partial z} - \frac{\partial A _ z}{\partial r}\biggr) \vec{e _ \theta} + \frac{1}{r} \biggl(\frac{\partial (r A _ \theta)}{\partial r} - \frac{\partial A _ r}{\partial \theta} \biggr) \vec{e _ z}
$$