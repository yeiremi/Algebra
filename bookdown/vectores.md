# Vectores

En este capítulo estudiaremos los vectores, objetos muy usados en la física para representar distintas nociones en las que se deben representar magnitudes,  direcciones y orientación, como lo son el desplazamiento, la velocidad, la fuerza, etc.  Sin embargo, se puden definir los vectores desde una perspectiva más abstracta, como los elementos de un espacio vectorial. En este capítulo nos centraremos en la noción más natural (como en la física) para desrrollar y mostrar las propiedades y operaciones de los vectores, estudiando los vectores en espacios euclideanos.

##Representación geométrica

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-1"><strong>(\#def:unnamed-chunk-1) </strong></span>	Un **vector** $v$ en $\mathbb{R}^{n}$ de dimensión $n$ es una n-tupla de $n$ números reales, de la forma $v=(a_{1}, a_{2},\cdots, a_{n})$. Llamaremos componente $i-$ésima al número $a_{i}$ ($1\leq i\leq n$).
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Nos centraremos en estuiar vectores en $\mathbb{R}^{2}$ o en $\mathbb{R}^{3}$. Los vectores en $\mathbb{R}^{2}$ o en $\mathbb{R}^{3}$ pueden representarse como un segmento de recta dirigido (una flecha) determinado por dos puntos en el espacio, $A$ de coordenadas $(x_{A},y_{A})$ y $B$ de coordenadas $(x_{B},y_{B})$, en los que uno es el origen del vector y el otro el extremo, en este caso se denota $\vec{AB}$ y sus coordenadas en el plano serían $\vec{AB}=(x_{B}-x_{A}, y_{B}-y_{A})$. también se puede denotar el vector con una letra minúscula $v=\vec{AB}$. La recta por la que pasa el vector es la **dirección** del vector.
</div>\EndKnitrBlock{remark}

La longitud del segmento de recta que define el vector (es decir, la flecha) es la **magnitud** del vector y se denota por $|\vec{AB}|$ (o $|v|$). La **dirección** del vector corresponde a la inclinación de la recta sobre la cual está el vector, esto es el ángulo que forma el vector con la horizontal. La **orientación** o **sentido** del vector representa el sentido en que se recorre el segmento de recta (determina hacia donde apunta la flecha). 

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Los vectores $\vec{AB}$ y $\vec{BA}$ tienen la misma magnitud, la misma dirección pero sentidos contrarios, por lo que $\vec{BA}=-\vec{AB}$. 
	Las coordenadas de un vector describen un rectángulo en el plano $\mathbb{R}^{2}$ en el que el vector es una de las diagonales.
</div>\EndKnitrBlock{remark}

\includegraphics[width=0.5\textwidth]{suma-vectores.eps}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-4"><strong>(\#def:unnamed-chunk-4) </strong></span>	Dado el vector $v$ de coordenadas $(x,y)$, **la magnitud** puede calcularse usando el teorema de pitágoras, con $|v|=\sqrt{x^{2}+y^{2}}$, la dirección es el **ángulo** $\theta$ que forma con el eje de las abscisas y se calcula con $\theta=\arctan(\frac{y}{x})$. El sentido es una noción referencial y se representan sentidos contrarios con los signos positivos ($+$) y negativos ($-$) (el signo $+$ suele omitirse)
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	En general, la **magnitud** de un vector $v$ en $\mathbb{R}^{n}$ es $|v|=\sqrt{\sum_{k=1}^{n}a_{k}^{2}}$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-6"><strong>(\#def:unnamed-chunk-6) </strong></span>	Dos **vectores** son **paralelos** si forman iguales ángulos con el eje de las abscisas. Es decir, $v_{1}=(x_{1},y_{1})$ y $v_{2}=(x_{2},y_{2})$ son paralelos si $\theta_{1}=\arctan(\frac{y_{1}}{x_{2}})=\theta_{2}=\arctan(\frac{y_{2}}{x_{2}})$.
</div>\EndKnitrBlock{definition}

##Operaciones vectoriales

Ya vimos que los vectores pueden representar conceptos físicos como lo son la distancia, la velocidad o la fuerza. Entonces es conveniente poder sumar estos objetos, para representar suma de distancias o suma de fuerzas, por ejemplo. También podemos pensar en multiplicar un vector por un escalar, como sería multiplicar la magnitud de una fuerza. En esta sección veremos que podemos definir varias operaciones entre vectores, sumar, restar y multiplicar vectores como lo hacemos con los números reales. Pero también definiremos operaciones propias de estos objetos, como lo son el producto punto y el producto cruz de vectores.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-7"><strong>(\#def:unnamed-chunk-7) </strong></span>	Dados los vectores $v_{1}=(x_{1},y_{1})$ y $v_{2}=(x_{2},y_{2})$, **la suma** de $v_{1}$ y $v_{2}$ está dada por la suma de las componentes correspondientes, es decir, $v_{1}+v_{2}=(x_{1}+x_{2},y_{1}+y_{2})$. En general, la suma de dos vectores $v=(a_{1}, a_{2},\cdots, a_{n})$ y $u=(b_{1}, b_{2},\cdots, b_{n})$ en $\mathbb{R}^{n}$ se define como $v+u=(a_{1}, a_{2},\cdots, a_{n})+(b_{1}, b_{2},\cdots, b_{n})=(a_{1}+b_{1},a_{2}+b_{2},\cdots a_{n}+b_{n})$.
</div>\EndKnitrBlock{definition}
La suma de vectores tiene las siguientes propiedades:

		(1) Es commutativa, es decir, $v_{1}+v_{2}=v_{2}+v_{1}$, para cuales quiera vectores $v_{1}, v_{2}$.
		
		(2) Es asociativa, esto es, $(v_{1}+v_{2})+v_{3}=v_{1}+(v_{2}+v_{3})$, para todo $v_{1}, v_{2}$ y $v_{3}$.
		
		(3) Existencia del elemento neutro o vector cero,  $v+\vec{0}=v$, para todo vector $v$. 
		
		(4) Para todo vector $v$, existe un vector $v´$ tal que $v+(v´)=\vec{0}$. 


\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-8"><strong>(\#def:unnamed-chunk-8) </strong></span>	Dado el vector $v=(x,y)$ y un escalar $\lambda\in\mathbb{R}$, **el producto** de $v$ **por un escalar** $\lambda$ está dada por la multiplicaión de cada una de las componentes por el escalar, es decir, $\lambda v=(\lambda x,\lambda y)$. En general, si $v=(a_{1},a_{2},\cdots, a_{n})$, entonces $\lambda v=(\lambda a_{1},\lambda a_{2},\cdots, \lambda a_{n})$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-9"><strong>(\#def:unnamed-chunk-9) </strong></span>	Dado el vector $v=(x,y)$ , el vector opuesto a $v$ es el vector $-v$ dado por el producto de $v$ por el escalar $-1$, es decir, $-v=-1 v=(-x,-y)$. En general, si $v=(a_{1},a_{2},\cdots, a_{n})$, entonces $-v=(-a_{1},-a_{2},\cdots, -a_{n})$.
</div>\EndKnitrBlock{definition}

El producto de vectores por un escalar tiene las siguientes propiedades:

	(1) Es commutativa, es decir, $\lambda v=v\lambda$, para cualquier vector $v$ y cualquier escalar $\lambda$.
	(2) Es distributiva, esto es, $\lambda(v_{1}+v_{2})=\lambda v_{1}+\lambda v_{2}$, para todo $v_{1}, v_{2}$ y todo $\lambda$.
	(3) Existencia del elemento neutro,  $1v=v$, para todo vector $v$. 

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-10"><strong>(\#def:unnamed-chunk-10) </strong></span>		Dados los vectores $v_{1}=(x_{1},y_{1})$ y $v_{2}=(x_{2},y_{2})$, **la resta** de $v_{1}$ y $v_{2}$ está dada por la suma de $v_{1}$ con el opuesto de $v_{2}$, es decir, $v_{1}-v_{2}=(x_{1},y_{1})-(x_{2},y_{2})=(x_{1}-x_{2},y_{1}-y_{2})$. En general, $v-u=(a_{1}, a_{2},\cdots, a_{n})-(b_{1}, b_{2},\cdots, b_{n})=(a_{1}-b_{1},a_{2}-b_{2},\cdots a_{n}-b_{n})$, cuando $v=(a_{1}, a_{2},\cdots, a_{n})$ y $u=(b_{1}, b_{2},\cdots, b_{n})$ son vectores de $\mathbb{R}^{n}$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-11"><strong>(\#exm:unnamed-chunk-11) </strong></span>	Dados los vectores $v_{1}=(10,2)$, $v_{2}=(-5,4)$ y $v_{3}=(-1,-2)$, entonces $$v_{1}+v_{2}=(10,2)+(-5,4)=(10-5,2+4)=(5,6),$$
	 $$v_{1}-v_{2}=(10,2)-(-5,4)=(10-(-5),2-4)=(15,-2) \mbox{ y}$$ $$v_{3}+v_{2}-v_{1}=(-1,-2)+(-5,4)-(10,2)=(-1-5-10,-2+4-2)=(-16,0).$$ También	 
	$$-2v_{1}=-2(10,2)=(-20,-4)\mbox{ y }$$ $$-2v_{1}+3v_{2}-v_{3}=-2(10,2)+3(-5,4)-1(-1,-2)=(-20-15+1,-4+12+2)=(-34,10).$$
</div>\EndKnitrBlock{example}

###Producto escalar y producto vectorial

Las operaciones que definiremos en esta parte son propias de los vectores. En la mayor parte de los conceptos nos remitiremos a los espacios $\mathbb{R}^{2}$ y $\mathbb{R}^{3}$.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-12"><strong>(\#def:unnamed-chunk-12) </strong></span>	Sean $v_{1}$ y $v_{2}$ vectores, el **producto escalar** de $v_{1}$ y $v_{2}$ es el producto de los módulos $|v_{1}|$ y $|v_{2}|$ y el coseno del ángulo que forman los vectores y se denota $v_{1}\cdot v_{2}$. Es decir, $v_{1}\cdot v_{2}=|v_{1}||v_{2}|\cos \theta$, donde $\theta$ es el \'angulo entre $v_{1}$ y $v_{2}$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	La proyección de $v_{1}$ sobre $v_{2}$ es $proy_{v_{2}} v_{1}=|v_{1}|\cos\theta$ donde $\theta$ es el ángulo que forman ambos vectores. Por lo tanto, $v_{1}\cdot v_{2}=|v_{2}| proy_{v_{2}} v_{1}$.
	También podemos calcular el producto escalar del siguiente modo: Sean $v_{1}=(x_{1}, y_{1})$ y $v_{2}=(x_{2}, y_{2})$ vectores, $v_{1}\cdot v_{2}=x_{1}x_{2}+y_{1}y_{2}$. En general, si $v_{1}$ y $v_{2}$ son vectores en $\mathbb{R}^{n}$ tales que $v_{1}=(x_{1},x_{2},\cdots, x_{n})$ y $v_{2}=(y_{1},y_{2},\cdots, y_{n})$, $v_{1}\cdot v_{2}=\sum_{i=1}^{n} x_{i}y_{i}$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-14"><strong>(\#exm:unnamed-chunk-14) </strong></span>	Dados los vectores $v=(\sqrt{3},1)$ y $u=(\frac{3}{2},\frac{3\sqrt{3}}{2})$, y sabiendo que el ángulo que ellos forman es 30\textdegree, entonces el producto escalar entre ellos $$v\cdot u=|v||u|\cos 30^{o}=2\cdot 3\cdot\frac{\sqrt{3}}{2}=3\sqrt{3}$$ ya que $|v|=\sqrt{\sqrt{3}^{2}+1^{2}}=\sqrt{4}=2$ y $|u|=\sqrt{(\frac{3}{2}^{2})+(\frac{3\sqrt{3}}{2})^{2}}=\sqrt{\frac{36}{4}}=3$. Note que si usamos la fórmula analítica podemos calcular el producto escalar $v\cdot u=(\sqrt{3}\cdot \frac{3}{2}) + (1\cdot \frac{3\sqrt{3}}{2})=3\sqrt{3}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-15"><strong>(\#exm:unnamed-chunk-15) </strong></span>	Dados los vectores $v=(1,2)$ y $u=(-3,4)$, el producto escalar es $v\cdot u=1\cdot (-3)+(2\cdot 4)$. Si queremos calcular el ángulo $\alpha$ entre los vectores, usamos la fórmula $v\cdot u=|v||u|\cos\alpha$, como $|v|=\sqrt{1^{2}+2^{2}}=\sqrt{5}$ y $|v|=\sqrt{(-3)^{2}+4^{2}}=5$, entonces $\cos\alpha=\frac{5}{\sqrt{5}\cdot 5}$, por lo tanto $\alpha=\arccos\frac{1}{\sqrt{5}}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Dos **vectores** $v_{1}, v_{2}$ son **perpendiculares** si y solo si forman un ángulo de $90^{o}$ entre ellos, esto lo denotamos con $v_{1}\perp v_{2}$. Como $\cos 90^{o}=0$ se puede ver que dos vectores no nulos son perpendiculares si y solo si el producto escalar entre ellos es cero. Es decir $v_{1}\perp v_{2}$ si y solo si $v_{1}\cdot v_{2}=0$, siempre que $u\neq 0$ o $v\neq 0$.
</div>\EndKnitrBlock{remark}

El producto escalar tiene las siguientes propiedades:

	(1) Conmutativa: Para todo par de vectores $v$ y $u$, se tiene $v\cdot u= u\cdot v$.
	(2) Distributiva respecto a la suma: Para cualesquiera vectores $u$, $v$ y $w$, se tiene que $u\cdot(v+w)=u\cdot v + u\cdot w$.
	(3) Asociatividad respecto al producto por un escalar: Para todo par de vectores $v$ y $u$ y todo escalar $\lambda$, se tiene que: $\lambda(u\cdot v)=(\lambda u)\cdot v=u\cdot (\lambda v)$.


\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-17"><strong>(\#def:unnamed-chunk-17) </strong></span>	Dados dos vectores, $u$ y $v$, el producto vectorial de $u$ y $v$ está definido como $u\times v=(|u||v| sen \theta) n$, donde $n$ es un vector de módulo uno (1) y perpendicular a los vectores $u$ y $v$, cuya dirección está dada por la regla de la mano derecha y $\theta$ es el ángulo entre los vectores $u$ y $v$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	La regla de la mano derecha consiste en dar el mismo sentido al producto vectorial de $u\times v$ que el avance de un sacacorchos al girar desde el vector $u$ al vector $v$. (insertar imagen)
	Desde el punto de vista geométrico, el módulo del producto vectorial corresponde al área del paralelogramo que forman los vectores $u$ y $v$ y las rectas paralelas a estos. (insertar imagen)
</div>\EndKnitrBlock{remark}

Otra forma de calcular el producto vectorial entre dos vectores $u=(a_{1},a_{2}, a_{3})$ y $v=(b_{1}, b_{2}, b_{3})$ es esta $u\times v=(a_{2}b_{3}-a_{3}b_{2}, a_{3}b_{1}-a_{1}b_{3}, a_{1}b_{2}-a_{2}b_{1})$, la cual resulta muy práctica en el caso de conocer las componetes de los vectores. 

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Si definimos el determinante de una matriz $2x2$ como sigue: 
	$$\left|  \begin{array}{ll} 
	a & b\\ 
	c & d
	\end{array} \right| = ad-bc$$, entonces el producto vectorial se pude calcular como sigue:\\
	$u\times v=(x,y,z)$ donde 
	$x=\left|  \begin{array}{ll} 
	a_{2} & a_{3}\\ 
	b_{2} & b_{3}
	\end{array} \right|$, $x=\left|  \begin{array}{ll} 
	a_{1} & a_{3}\\ 
	b_{1} & b_{3}
	\end{array} \right|$, $x=\left|  \begin{array}{ll} 
	a_{1} & a_{2}\\ 
	b_{1} & b_{2}
	\end{array} \right|$.\\
	
	En el capítulo de matrices veremos mas formalmente el concepto de determinante de una matriz.
</div>\EndKnitrBlock{remark}

Note que $u\cdot (u\times v)=a_{1}(a_{2}b_{3}-a_{3}b_{2})+ a_{2}(a_{3}b_{1}-a_{1}b_{3})+ a_{3}(a_{1}b_{2}-a_{2}b_{1})=0$ lo que implica que $u\perp u\times v$. De forma análoga se muestra que $v\perp u\times v$.

El producto vectorial tiene las siguientes propiedades:
Sean $u,v, w\in \mathbb{R}^{3}$ vectores en el espacio y $\lambda\in \mathbb{R}$ un escalar, se tiene que:

	(1) $u\times \vec{0}=\vec{0}$,
	(2) $u\times u=\vec{0}$,
	(3) $u\times v= -(v\times u)$,
	(4) $\lambda (u\times v)= (\lambda u)\times v=u\times (\lambda v)$,
	(5) $u\times (v+w)=(u\times v) + (u\times w)$,
	(6) $u\times (v\times w)=(u\cdot w)v-(u\cdot v)w$,
	(7) $u\cdot (v\times w)=(u\times v)\cdot w$.


Por último definiremos el *producto mixto* o *triple producto escalar*:

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-20"><strong>(\#def:unnamed-chunk-20) </strong></span>	Dados los vectores $u,v, w\in \mathbb{R}^{3}$, el **producto mixto** es la operación que denotaremos $[u,v,w]=u\cdot(v\times w)$.
</div>\EndKnitrBlock{definition}

El producto mixto tiene las siguientes propiedades:
Sean $u,v, w,\in \mathbb{R}^{3}$ vectores en el espacio, se tiene que:

	(1) $[u,v,w]=[v,w,u]=[w,u,v]$,
	(2) $[u,v,w]=u\cdot(v\times w)=v\cdot(w\times u)=w\cdot(u\times v)$,
	(3) $[u,v,w]=0$ si y solo si $u$, $v$ y $w$ son coplanares,
	(4) es trilineal, es decir: 
			(i) $[(\lambda u+ \delta u'),v,w]=[\lambda u,v,w]+[\delta u',v,w]$, para cualquier vector $u'$ y cualesquiera escalares $\lambda$ y $\delta$.
		  (ii) $[u,(\lambda v+ \delta v'),w]=[u,\lambda v,w]+[u,\delta v',w]$, para cualquier vector $v'$ y cualesquiera escalares $\lambda$ y $\delta$.
		  (iii) $[u,v,(\lambda w+ \delta w')]=[u,v,\lambda w]+[u,v,\delta w']$, para cualquier vector $w'$ y cualesquiera escalares $\lambda$ y $\delta$.
  (5) es antisimétrica: $[u,v,w]=-[v,u,w]=-[u,w,v]=[w,v,u]$.


\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Interpretación geométrica del producto mixto: así como el módulo del producto vectorial $u\times v$ corresponde al área del paralelogramo que forman los vectores $u$ y $u$; el producto mixto $[u,v,w]$ es igual al volumen del paralelepípedo que ellos forman. Esto es fácil de demostrar pues el  volumen $V$ es igual a la base del paralelogramo, que es igual al módulo del producto vectorial, por la altura $h$ que es igual a $|w|\cos\theta$, por lo tanto $V=A h=|(u\times v)||w|\cos\theta=|(u\times v)\cdot w|=|[u,v,w]|$.
	(INSERTAR IMAGEN)
</div>\EndKnitrBlock{remark}

##Rectas y Planos


###Rectas en el espacio

En esta sección estudiaremos las rectas como objetos en el espacio $\mathbb{R}^{3}$. Una recta es un conjunto infinito de puntos que siguen una determinada  dirección y que pasa por un punto conocido en el espacio. Más formalmente:

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-22"><strong>(\#def:unnamed-chunk-22) </strong></span>	Dado un punto $P(x_{0},y_{0},z_{0})$ y un vector $u=(a,b,c)$, la recta que pasa por $P$ y está en la misma dirección que el vector $u$, es el conjunto de puntos $X(x,y,z)$ que cumplen que $\vec{PX}=\lambda u$, para algún número real $\lambda$, es decir, el vector $\vec{PX}$ es un múltiplo escalar del vector $u$. En este caso el vector $u$ se llamará **vector director** de la recta.
</div>\EndKnitrBlock{definition}

Note que la ecuación $\vec{PX}=\lambda u$ es equivalente a $X=P+\lambda u$, es decir 

\begin{equation}
(x,y,z)=(x_{0},y_{0},z_{0})+\lambda(a,b,c)
(\#eq:ecvecesp)
\end{equation}

a la que llamaremos **ecuación vectorial** de la recta.

De la ecuación vectorial, podemos deducir que un punto $X(x,y,z)$ pertenece a la recta si y solo si cumple simultaneamente las ecuaciones para cada una de sus componentes del vector:

\begin{equation}  
\left\{ \begin{array}{ll}
x=&x_{0}+\lambda a\\
y=&y_{0}\lambda b\\
z=&z_{0}\lambda c  
\end{array}
\right.
(\#eq:ecparesp)
\end{equation}
Estas se llaman **ecuaciones param\'etricas** de la recta.

Note que el escalar $\lambda$ es el mismo para todas las ecuaciones anteriores, para cada punto $X(x,y,z)$ sobre la recta. Si despejamos $\lambda$ de las ecuaciones paramétricas e igualamos obtenemos la **ecuación continua** de la recta: 

\begin{equation}
\frac{x-x_{0}}{a}=\frac{y-y_{0}}{b}=\frac{z-z_{0}}{c}
(\#eq:ecconesp)
\end{equation}

Otra manera de escribir esta cadena de desigualdades es como este sistema de ecuaciones:
$$\left\{ \begin{array}{ll}
\frac{x-x_{0}}{a}=&\frac{y-y_{0}}{b}\\
\frac{x-x_{0}}{a}=&\frac{z-z_{0}}{c}  
\end{array}
\right.$$ 

O equivalentemente, agrupando términos y renombrando los coeficientes, podemos escribirlo como:

\begin{equation}
\left\{ \begin{array}{ll}
Ax+By+Cz+D=&0\\
A'x+B'y+C'z+D'=&0  
\end{array}
\right.
(\#eq:eccaresp)
\end{equation}

Estás últimas son las **ecuaciones implícitas** de la recta o **ecuaciones cartesianas**, las cuales representan la intersección de dos planos (veremos este tema más adelante).

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-23"><strong>(\#exm:unnamed-chunk-23) </strong></span>	La recta que pasa por el punto $P(1,0,1)$ y tiene la dirección del vector $u=(4,5,-1)$ tiene la siguiente ecuación vectorial:  $(x,y,z)=(1,0,1)+\lambda(4,5,-1)$.
	La ecuaciones paramétricas son:
	$$\left\{ \begin{array}{ll}
	x=&1+4\lambda\\
	y=&5\lambda\\
	z=&1-\lambda
	\end{array}
	\right.$$ 
	De dónde se tiene que la ecuación continua es $\frac{x-1}{4}=\frac{y}{5}=\frac{z-1}{-1}$ y de acá se sigue que 
		$$\left\{ \begin{array}{ll}
		\frac{x-1}{4}=&\frac{y}{5}\\
		\frac{x-1}{4}=&\frac{z-1}{-1}
		\end{array}
		\right. \Leftrightarrow
		\left\{ \begin{array}{ll}
		5x-4y-5=&0\\
		x-4z-5=&0
		\end{array}
		\right.$$ 
	corresponde a la ecuación cartesiana de la recta.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-24"><strong>(\#exm:unnamed-chunk-24) </strong></span>	La recta que pasa por los puntos $A(1,0,1)$ y $B(0,1,1)$ viene dada por la ecuación vectorial  $(x,y,z)=(1,0,1)+\lambda(-1,1,0)$, ya que un vector director es $\vec{AB}$.
	La ecuaciones paramétricas son:
	$$\left\{ \begin{array}{ll}
	x=&1-\lambda\\
	y=&\lambda\\
	z=&1
	\end{array}
	\right.$$ 
	Por lo tanto la ecuación cartesiana es 
	$$\left\{ \begin{array}{ll}
	1-x=&y\\
	z=&1
	\end{array}
	\right. \Leftrightarrow
	\left\{ \begin{array}{ll}
	x+y-1=&0\\
	z-1=&0
	\end{array}
	\right.$$ 
	Note que la ecuación $z=1$ es el plano paralelo al plano $XY$ con altura en uno (1).</div>\EndKnitrBlock{example}
**Posici\'on relativa de dos rectas en el espacio.**

Dos rectas en el espacio pueden intersectarse o no. En el caso que se intersecten, estas forman un ángulo entre ellas pues estarían en el mismo plano, este ángulo pudiese ser un ángulo recto, lo que las haría perpendiculares entre sí. En el caso que no se intersecten, puede que sean paralelas entre sí o simplemente cruzarse sin tocarse (también se les dice alabeadas). Veamos esto en detalle:

Dadas dos rectas $\mathit{l}_{1}$ y $\mathit{l}_{2}$ de ecuacines $P+\lambda u$ y $Q+\delta v$, con $\lambda, \delta\in\mathbb{R}$, se tiene que:

	(1) $\mathit{l}_{1}$ y $\mathit{l}_{2}$ son paralelas si y solo si sus vectores directores $u$ y $v$ son paralelos. Lo denotamos por $\mathit{l}_{1}\parallel \mathit{l}_{2}$.
	(2) $\mathit{l}_{1}$ y $\mathit{l}_{2}$ son perpendiculares (u ortogonales) si y solo si sus vectores directores $u$ y $v$ lo son. Esto lo denotamos por $\mathit{l}_{1}\perp\mathit{l}_{2}$.
	(3) $\mathit{l}_{1}$ y $\mathit{l}_{2}$ se intersectan si y solo si $[u,v,\vec{PQ}]=(u\times v)\cdot \vec{PQ}=0$, ya que el vector $u\times v$ es perpendicular al plano que forman las rectas y como el vector $\vec{PQ}$ pertenece a este plano, es también perpendicular a $u\times v$.
	(4) $\mathit{l}_{1}$ y $\mathit{l}_{2}$ se cruzan sin intersectarse si y solo si $[u,v,\vec{PQ}]=(u\times v)\cdot \vec{PQ}\neq0$. No son paralelas y no pertenecen al mismo plano.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-25"><strong>(\#exm:unnamed-chunk-25) </strong></span>	Dadas las rectas $\mathit{l}_{1}: (0,1,2)+\lambda(1,1,1)$, $\lambda\in \mathbb{R}$ y 
	$\mathit{l}_{2}:\left\lbrace \begin{array}{ll}
	x=& \delta\\
	y=& \delta\\
	z=& 0
	\end{array}
	\right.$, con $\delta\in\mathbb{R}.$
Se tiene que el vector director de $\mathit{l}_{1}$ es $(1,1,1)$ y el vector director de $\mathit{l}_{2}$ es $(1,1,0)$ no son paralelos, por lo tanto las rectas no son paralelas. Tampoco son perpendiculares ya que $u\cdot v=|u||v|\cos\theta$, donde $\theta$ es el ángulo que forman los vectores $u$ y $v$. Por lo tanto $\cos\theta=\frac{u\cdot v}{|u||v|}=\frac{\sqrt{6}}{3}$, por lo tanto $\theta\neq0$. las rectas pueden ser rectas que se intersecten o que solo se crucen, para ver esto calculemos $[u,v,\vec{PQ}]={(1,1,1)\times(1,1,0)}\cdot (0,-1,-2)=(-1,1,0)\cdot(0,-1,-2)=0-1+0=-1\neq0$ por lo tanto las rectas se cruzan (no se intesectan).
</div>\EndKnitrBlock{example}


###Rectas en el plano

En esta parte describiremos como son las rectas en el plano cartesiano $\mathbb{R}^{2}$. Veremos como son las ecuaciones de las rectas en plano. Las características de rectas paralelas y perpendiculares así como el punto de intersección de dos rectas. 

De la sección anterior tenemos que una recta en $\mathbb{R}^{2}$ está inequivocamente determinada por un punto en el plano $P(x_{0},y_{0})$ y un vector director $u=(a,b)$. La **ecuación vectorial** de la recta es $\vec{PX}=\lambda u$, esto es $(x-x_{0},y-y_{0})=\lambda(a,b)$, es decir

\begin{equation}
(x,y)=(x_{0},y_{0})+\lambda(a,b)
(\#eq:ecvecpla)
\end{equation}

de donde se obtiene $(x,y)=(x_{0},y_{0})+\lambda(a,b)$, por lo tanto 
$$\left\lbrace \begin{array}{ll} 
x=&x_{0}+a\lambda\\ 
y=&y_{0}+b\lambda
\end{array} \right.$$
De donde podemos obtener $\frac{x-x_{0}}{a}=\frac{y-y_{0}}{b}\Leftrightarrow b(x-x_{0})=a(y-y_{0})$. Si $a\neq 0$ se tiene que $y=\frac{b}{a}x+(y_{0}-\frac{b}{a}x_{0})$.
Renombrando los coeficientes de la última ecuación, obtenemos la conocida **ecuación explícita** de la recta en el plano 

\begin{equation}
y=mx+n
(\#eq:ecexppla)
\end{equation}

donde el coeficiente $m$ corresponde a la **pendiente de la recta** (la inclinación) y es igual a la tangente del ángulo que forma la recta con el eje horizontal (abscisas o eje $x$). Note que si el vector director no es paralelo al eje vertical (las ordenadas o eje $Y$), entonces $a\neq 0$ en \ref{ecvecpla} y por lo tanto podemos dividir por $a$. Además, si $x=0$, se tiene que $y=m(0)+n$, es decir $y=n$, de donde se sigue que el **punto de corte de la recta con el eje de las abscisas** (o eje $Y$) es el coeficiente $n$ de la ecuación explícita \@ref{eq:ecexppla}. Por otro lado el **punto de corte de la recta con el eje de las ordenadas** (eje $X$) es un punto cuya segunda coordenada es cero, esto es $(x,0)$, por lo tanto $0=mx+n$, entonces $x=\frac{n}{m}$.
También podemos escribir la **ecuación implícita o cartesiana** de la recta renombrando los coeficientes y reordenando los términos de la ecuación \@ref{eq:ecvecpla} para obtener 

\begin{equation}
Ax+By+C=0
(\#eq:ecimppla)
\end{equation}

Si sabemos que una recta $y=mx+n$ pasa por dos puntos conocidos del plano $A(x_{1},y_{1})$ y $B(x_{2},y_{2})$, podemos calcular la pendiente de la recta calculando la tangente del ángulo que forma el segmento de recta que une los puntos $A$ y $B$ como lo muestra la figura (INSERTAR FIGURA). De este modo 

\begin{equation}
m=tang(\alpha)=\frac{y_{2}-y_{1}}{x_{1}-x_{2}}
(\#eq:pendiente)
\end{equation}

La ecuanción antes descrita es cierta para todo par de puntos sobre la recta, por lo tanto, si $A(x_{0},y_{0})$ es un punto conocido y $X(x,y)$ es un punto arbitrario sobre la recta, se tiene que $m=\frac{y-y_{0}}{x-x_{0}}$. Si conocemos la pendiente de la recta, podemos despejar $y$ en término de la pendiente y las coordenadas del punto conocido, obteniendo así la **ecuación punto-pendiente** de la recta:

\begin{equation}
y=m(x-x_{0})+y_{0}
(\#eq:puntopend)
\end{equation}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-26"><strong>(\#exm:unnamed-chunk-26) </strong></span>	Para hallar la ecuación de la recta que pasa por el punto $A(3,1)$ y tiene pendiente $m=\frac{1}{2}$ usamos la ecuación punto pediente \@ref(eq:puntopend),
	$y=\frac{1}{2}(x-3)+1$ por lo tanto $y=\frac{1}{2}x-\frac{1}{2}$. Reagrupando términos y multiplicando por $2$, obtenemos la ecuación implícita \@ref(eq:ecimppla): $x-2y-1=0$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-27"><strong>(\#exm:unnamed-chunk-27) </strong></span>	Dada la ecuación cartesiana de la recta $5x-3y+1=0$, podemos hallar la pendiente de la recta despejando $y$ de la ecuación cartesiana, de la siguiente forma: $y=\frac{5}{3}x+\frac{1}{3}$. De donde se sigue que la pendiente es $m=\frac{5}{3}$. Además, directamente de la ecuación explícita, podemos decir que el punto de corte con el eje $Y$ es $n=\frac{1}{3}$. Para hallar el punto de corte con el eje $X$, despejamos $x$ de $0=\frac{5}{3}x+\frac{1}{3}$, así $x=\frac{-1}{5}$.
</div>\EndKnitrBlock{example}
Dos rectas en plano pueden ser **rectas paralelas**, en ese caso tienen la misma pendiente (forman el mismo ángulo con el eje $X$), es decir, si la recta $\mathit{l}_{1}$ tiene ecuación $y=mx+n$ y la recta $\mathit{l}_{2}$ tiene ecuación $y=px+q$, entonces $\mathit{l}_{1}$ es paralela a $\mathit{l}_{2}$ si y solo si $m=p$, esto se denota $\mathit{l}_{1} \parallel \mathit{l}_{2}$.

Si dos rectas $\mathit{l}_{1}$ y $\mathit{l}_{2}$ de ecuaciones $y=mx+n$ y $y=px+q$ respectivamente, forman un ángulo de $90^{o}$ entre ellas se dice que son **perpendiculares** y se denota $\mathit{l}_{1} \perp \mathit{l}_{2}$, en este caso se puede ver que las pendientes guardan la siguiente relación: $mp=-1$.

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Note que si una recta es horizontal, su pendiente es igual a cero, esto es $y=0x+n$ y cualquier recta perpendicular a ella es paralela al eje $Y$ y por lo tanto no es función.
</div>\EndKnitrBlock{remark}

Dos rectas no paralelas $\mathit{l}_{1}$ y $\mathit{l}_{2}$ de ecuaciones $y=mx+n$ y $y=px+q$ respectivamente, se intersectan en un punto del plano $(x_{0},y_{0})$, por lo tanto satisface ambas ecuaciones simultaneamente, es decir, $y_{0}=mx_{0}+n$ y $y_{0}=px_{0}+q$. Luego $mx_{0}+n=y_{0}=px_{0}+q$ por lo tanto $mx_{0}-px_{0}=q-n\Leftrightarrow x_{0}=\frac{q-n}{m-p}$ y así, $y_{0}=m(\frac{q-n}{m-p})+n$. En este caso el punto de intersección entre las rectas es $$\left( \frac{q-n}{m-p},m(\frac{q-n}{m-p})+n\right) .$$

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-29"><strong>(\#exm:unnamed-chunk-29) </strong></span>	Las rectas $\mathit{l}_{1}:y=2x+3$ y $\mathit{l}_{2}:y=2x-1$ son rectas paralelas. Y son perpendiculares a $\mathit{l}_{3}: y=-\frac{1}{2}x+1$. Además, el punto de intersección entre $\mathit{l}_{1}$ y $\mathit{l}_{2}$ es $x_{0}=\frac{1-3}{2+\frac{1}{2}}=\frac{-4}{5}$ y $y_{0}=2(\frac{-4}{5})+3=\frac{7}{5}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-30"><strong>(\#exm:unnamed-chunk-30) </strong></span>	La recta perpendicular a $\mathit{l}_{1}:\frac{-2}{3}x+3$ que pasa por el punto $A(-2,1)$ tiene por ecuación $y=\frac{3}{2}(x-(-2))+1$ es decir $y=\frac{-3}{2}x+4$.
</div>\EndKnitrBlock{example}