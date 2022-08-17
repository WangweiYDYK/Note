形变映射$\vec x = \vec\phi(\vec X)$  $R^{3}\rightarrow R^{3}$, $\vec x$ 为形变后位置， $\vec X$为形变前位置

变形梯度张量
$$\mathbf F : = \frac { \partial ( \phi _ { 1 } , \phi _ { 2 } , \phi _ { 3 } ) } { \partial ( X _ { 1 } , X _ { 2 } , X _ { 3 } ) } = \left( \begin{array} { l l l } { \partial \phi _ { 1 } / \partial X _ { 1 } } & { \partial \phi _ { 1 } / \partial X _ { 2 } } & { \partial \phi _ { 1 } / \partial X _ { 3 } } \\ { \partial \phi _ { 2 } / \partial X _ { 1 } } & { \partial \phi _ { 2 } / \partial X _ { 2 } } & { \partial \phi _ { 2 } / \partial X _ { 3 } } \\ { \partial \phi _ { 3 } / \partial X _ { 1 } } & { \partial \phi _ { 3 } / \partial X _ { 2 } } & { \partial \phi _ { 3 } / \partial X _ { 3 } } \end{array} \right)$$

$\Psi$ $[\phi; \vec x]$ 是能量密度函数，衡量在点 $\vec X$周围的无穷小域dV上每个单位体积的应变能, $\phi$是形变映射 。因此整个域$\Omega$中的形变能量
$$E[\phi] = \int_\Omega \Psi[\phi; \vec X]d\vec X$$
对任意点$\vec X_*$，由于$\Psi[\phi; \vec X_*]$是周围的无穷小域dV上每个单位体积的应变能，因此可对dV内的形变通过一阶泰勒展开进行近似操作
$$\phi ( \vec { X } ) \approx \phi ( \vec { X } _ { * } ) + \frac { \partial \phi } { \partial \vec { X } } | _ { \vec { X } _ { * } } ( \vec { X } - \vec { X } _ { * } ) = \vec { x } _ { * } + \mathbf F ( \vec { X } _ { * } ) ( \vec { X } - \vec { X } _ { * } )$$
$$= \underbrace { \mathbf F ( \vec { X } _ { * } ) } _ { \mathbf F _ { * } } \vec { X } + \underbrace { \vec { x } _ { * } - \mathbf F ( \vec { X } _ { * } ) \vec { X } _ { * } } _ { \vec { t } } = \mathbf F _ { * } \vec { X } + \vec { t }$$

对于连续介质，使用$\vec f(\vec X)$代表点$\vec X$周围无穷小域dV上每单位体积的力，那么，对于任意$A\subseteq \Omega$,有
$$\vec f_{aggregate}(A) = \int_A \vec f(\vec X)d\vec X$$
需要注意的是该公式不适合描述对材料边缘所施加的力。对于一个弹性体进行均匀的压缩($\vec\phi(\vec X) = \alpha\vec X, \alpha<1$)，其表面会有反作用，在这里定义$\vec\tau(\vec X)$为表面力密度函数来衡量每单位面积上的力，那么有
$$\vec f_{aggregate}(B) = \oint_B \vec\tau(\vec X)d\vec X$$ 

1st Piola-Kirchhoff stress tensor $\mathbf P$ 是一个3*3矩阵，对于hyperelastic material，$\mathbf P$可描述为deformation gradient的函数
$$\mathbf{P}(\mathbf{F})=\partial \Psi(\mathbf{F}) / \partial \mathbf{F}$$
对于边界点$\vec X\in\partial\Omega$
$$\vec\tau(\vec X) = -\bold{P}\cdot\vec N$$
而对于内部点$\vec X$，有
$$\vec f(\vec X)=\bold{div}_{\vec X}\bold{P}(\vec X)$$
或者
$$f_{i}=\sum_{j=1}^{3} P_{i j, j}=\frac{\partial P_{i 1}}{\partial X_{1}}+\frac{\partial P_{i 2}}{\partial X_{2}}+\frac{\partial P_{i 3}}{\partial X_{3}}$$