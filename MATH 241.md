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
