### 12.2
For a vector $\vec{a} = <a_1, a_2, ..., a_n>$, its length $|\vec{a}|=\sqrt{(a_1)^2+(a_2)^2+...+(a_n)^2}$ 
Vectors length of 1 are called **unit vectors or standard basis vectors**
### 12.3 Dot Product
$$\vec{a} = <a_1, a_2, a_3>\ \vec{b}= <b_1, b_2, b_3>,\ a \cdot b = a_1b_1 + a_2b_2 + a_3b_3 = |a||b|\cdot \cos{\theta}$$
$\theta$ is the angle between $\vec{a}$ and $\vec{b}$. Note that this is a **scalar product**.
Properties for vectors a, b, c
	$a \cdot a = |a|^2$
	其余定律与一般乘法交换律无异
Combine with Law of Cosine
	assume triangle OAB and we treat O as origin
	$$|AB|^2 = |OA|^2 + |OB|^2 - 2|OA||OB|\cos{\theta}$$
	Now $|OA| = |\vec{a}|,\ |OB| = |\vec{b}|, |AB| = |\vec{a} - \vec{b}|$
	$$|a-b|^2 = |a|^2 + |b|^2 - 2|a||b|\cos{\theta}$$
	By doing bunch of work you can see that it proves that $a \cdot b = |a||b| \cdot \cos{\theta}$ 

### 12.4 Cross Product
Suppose there are two vectors $\vec{a}$ and $\vec{b}$ in $R^3$, and there is a nonzero vector $\vec{c}$ s.t. $\vec{c} \perp \vec{a}\ and\ \vec{b}$. 
The cross product of a and b is c.
Using determinant to remember
$$a \times b = \left| \begin{matrix} i&j&k \\ a_1&a_2&a_3 \\ b_1&b_2&b_3\end{matrix} \right| =
\left| \begin{matrix} a_2&a_3 \\b_2&b_3\end{matrix} \right|i - 
\left| \begin{matrix} a_1&a_3 \\b_1&b_3\end{matrix} \right|j +
\left| \begin{matrix} a_1&a_2 \\b_1&b_2\end{matrix} \right|k
$$
Properties
	$(a \times b)\cdot a = 0$. Since $a \times b \perp a$
	![[Pasted image 20260920215339.png]]
	$a \times b$ and $b \times a$ are vectors with opposite directions
	If $0 \leq \theta \leq \pi$ is the angle between a and b, then $|a \times b| = |a||b|\sin{\theta}$ 
	If $\sin{\theta}=0$ then $|a \times b|$ = 0

From $|a \times b| = |a||b|\sin{\theta}$ we can see that the cross product can get Area of a parallelogram like
![[Pasted image 20260920215957.png]]
If there are three vectors that makes a **parallelepiped** (a solid made of six parallelograms), you can find its volume by $|(a \times b)\times c|$  imagining c is the third line
	$(ka)\times b=k(a\times b) = a\times(kb)$
	$a \times (b+c) = a\times b = a \times c$ 
	$a \cdot (b \times c) = (a \times b) \cdot c$ 
	$a \times (b \times c) = (a \cdot c)b - (a \cdot b)c$ 

For getting the distance D between a plane and a point, we must first understand the concept of **vector projection**.
![[Pasted image 20260921093107.png|333]]
As shown in the graph, component of vector b on a is $comp_ab = \frac{a\cdot b}{|\vec{a}|}$.
$$a \cdot b = |a||b|\cos{\theta} = |a||b|\cdot \frac{comp_ab}{|b|}$$
Therefore, it needs to be divided by |a|

### 12.5 Lines and Planes
$P_0(x_0, y_0, z_0)$ is an arbitrary point at line $L$, a vector $\vec{v} = <a,b,c>,\ v \parallel L$, $r_0 = <x_0,y_0,z_0>$ and $r = <x,y,z>$ are the position vectors of $\vec{OP_0}$ and $\vec{OP}$. Let $t$ be an input, now
$$r = r_0 + tv$$
$$<x,y,z> = <x_0 + ta, y_0 + tb, z_0 + tc>$$
$$t = \frac{x-x_0}{a} = \frac{y-y_0}{b} = \frac{z-z_0}{c}$$
$r$ now is an equation that describes $L$ by showing every points at $L$.

For planes, we need an arbitrary point $P(x,y,z)$ at the plane, and a normal vector $n = <a,b,c>$. Assume there are two vectors $r$ and $r_0$ be the position vectors of $P$ and $P_0$, now
$$n\cdot (r - r_0) = 0 \to n\cdot r = n\cdot r_0$$
$$<a,b,c>\cdot <x-x_0,y-y_0,z-z_0> = 0$$
$$a(x-x_0) + b(y-y_0) + c(z-z_0) = 0 \to ax + by + cz = ax_0 + by_0 + cz_0$$
**Important: P is an arbitrary point, meaning that r - r_0 can narrow down n to one direction**

Questions: given two planes (two equations), find the angle between them, and the equation for intersection line
	since we know normal vectors of both planes,  we can use $n_1 \cdot n_2 = |n_1||n_2| \cos{\theta}$ to find it
	For line equation
		since they are both linear equations, we can use substitution to get a point that is at both planes. Then, we can get a vector parallel to the line by $n_1 \times n_2$ since the line is perpendicular to both planes. Then apply the point and the vector to equation

Finding distance D between a point and a plane
	
### 12.6 Cylinders and Quadric Surfaces
Parabolic Cylinder
	e.g. $y=ax^2 + bx +c$ is a parabolic cylinder. This is a parabola at xy-plane, and the parabola extends along z-axis (the axis that doesn't show up)
	![[Pasted image 20260905101417.png|228]]
Ellipsoid(椭圆)
	$a(x-x_0)^2 + b(y-y_0)^2 + c(z-z_0)^2 = 1$ Then $(x_0, y_0, z_0)$ is the center.
	![[Pasted image 20260905102211.png|194]]
Elliptic Paraboloid
	$z = a(x-x_0)^2 + b(y-y_0)^2 + z_0$ 
	We can see that: if a,b > 0, then the shape opens up; if a,b < 0, then the shape opens down
	![[Pasted image 20260905105105.png|274]]
Hyperboloid of one sheet, Hyperboloid of two sheets, Double cone
	$x^2 + y^2 -z^2 =c$ 
	If c = 0, there will be two cones pointing tip-to-tip, and the center axis will be the z-axis.
	If c > 0, there will be hyperboloid of one sheet (one continuous shape)
	If c < 0, there will be hyperboloid of two sheets (two shapes)
	![[Recording 2026-09-05 110936.mp4]]

### 14.2
To check the limit that contains multiple variables, test it by approaching the limit from each single variable
	e.g. $\lim_{(x,y)\to (0,0)}\frac{x^4-16y^2}{x^2+8y^2}$ 
	$\lim_{x \to 0} f(x,y) = -2$
	$\lim_{y \to 0} f(x,y) = 0$
	Therfore, the limit DNE.

### Using Epsilon-delta language
Consider the function $f: R^2 \to R$ given by $f(x,y) = \frac{xy^2}{\sqrt{x^2+y^2}}$ for $(x,y) \neq 0$ 
In this problem, you will show $\lim_{h \to 0}f(h) =0$ 
	For $\epsilon = \frac{1}{2}$, find some $\delta > 0$ so that when $0 < |h|<\delta$ we have $|f(h)|<\epsilon$.
	$\delta > |h| = \sqrt{x^2 +y^2}$
	$|f(h)|=\frac{|x|y^2}{\sqrt{x^2+y^2}}$ 
	We know that $x < \sqrt{x^2+y^2}$, then $\frac{x}{\sqrt{x^2+y^2}} \leq 1$, then $\frac{|x|y^2}{\sqrt{x^2+y^2}} \leq y^2$.
	$y^2 \leq x^2+y^2 = |h|^2$ 
	$|f(h)| \leq y^2 \leq x^2+y^2 = |h|^2$ 
	Now we treat $|h|^2$ as $\delta^2$ 
	$\delta^2 = \epsilon \to \delta = \frac{1}{\sqrt{2}}$ 
	Now show that $\lim_{h \to 0} f(h)=0$. That is, given an arbitrary $\epsilon > 0$, find a $\delta >0$ so that when $0<|h|<\delta$ we have $|f(h)|<\epsilon$.
	From the previous, we know that $|f(h)|<|h|^2$. If $|h|^2<\epsilon$, then  $|f(h)|<\epsilon$. $|h| < \sqrt{\epsilon}$, so we set $\delta = \sqrt{\epsilon}$, which is a valid choice for every $\epsilon > 0$.
	For this kind of question, _"Give me any desired accuracy ϵ for the output, and I'll tell you how much accuracy δ I need in the input."_ 

Tangent Plane Formula: 
$$z- z_0 = f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y - y_0)$$
Linearization Formula
$$L(x,y) = f(a,b) + f_x(a,b)(x-a) + f_y(a,b)(y-b)$$
Get Total Differential
$$z = f(x,y)$$
$$dz = f_x(x,y)dx + f_y(x,y)dy$$
Taking Derivatives
$$g(r,s) = f(x,y) = f(9r-s, s^2 -3r),\ x(r,s) = 9r -s,\ y(r,s) = s^2 - 3r$$
$$g_r = f_x \cdot \frac{\partial x}{\partial r} + f_y\cdot \frac{\partial y}{\partial r}$$
This is an application of chain rule. We take the partial derivative of f w.r.t. x and y, and we take partial derivatives from x and y.

![[Pasted image 20260916225607.png]]
$$\frac{\partial z}{\partial s} = z_x\cdot x_s + z_y\cdot y_s = z_x\cdot 2s + z_y\cdot 7r$$
	for the second derivative, notice that both $z_x$ and $z_y$ contain both x and y
$$\frac{\partial ^2 z}{\partial r \partial s} = 2s\cdot (z_{xx}\cdot x_r+z_{xy} \cdot y_r) + (z_{yx}\cdot x_r + z_{yy} \cdot y_r) \cdot 7r + 7\cdot z_y$$
$$\frac{\partial ^2 z}{\partial r \partial s} = 2s\cdot (z_{xx}\cdot 2r+z_{xy} \cdot 7s) + (z_{yx}\cdot 2r + z_{yy} \cdot 7s) \cdot 7r + 7\cdot z_y$$
$$\frac{\partial ^2 z}{\partial r \partial s} = 4rs\cdot z_{xx}+14(r^2+s^2)\cdot z_{xy} + 49rs\cdot z_{yy} + 7z_y$$
