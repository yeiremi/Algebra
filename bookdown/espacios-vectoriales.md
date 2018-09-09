# Espacios vectoriales
En este capítulo estudiaremos los espacios vectoriales, un concepto abstrato de una estructura cerrada bajo combinaciones lineales. Veremos que las matrices son objetos muy útiles para trabajar en espacios vectoriales. Por esta razón estudiaremos algunos aspectos básicos de estos objetos. Como motivación para el estudio de las matrices iniciaremos el capítulo estudiando las ecuaciones lineales y poco a poco iremos acercándonos al estudio de los espacios vectoriales.

## Ecuaciones lineales
En este sección estudiaremos las ecuaciones lineales como motivación para el estudio de los conceptos iniciales de matrices. Además estudiaremos las operaciones básicas de suma y producto por un escalar así como el producto de matrices. Luego estudiaremos el concepto de invertibilidad de matrices, para ello definiremos las operaciones elementales por filas. 

Sea $\mathbb{F}$ un cuerpo. Supongamos que queremos hallar $n$ escalares (elementos del cuerpo $\mathbb{F}$) $x_{1},x_{2}, \cdots, x_{n}$ que satisfagan las condiciones:
\begin{equation}
	\begin{array}{ccccc}
		A_{11}x_{1}+&A_{12}x_{2}+&\cdots +&A_{1n}x_{n}=&b_{1}\\
		A_{21}x_{1}+&A_{22}x_{2}+&\cdots +&A_{2n}x_{n}=&b_{2}\\
		\vdots& &\ddots& \vdots& \vdots	\\
		A_{m1}x_{1}+&A_{m2}x_{2}+&\cdots +&A_{mn}x_{n}=&b_{m}
	\end{array}
	(\#eq:sistemalineal)
\end{equation}
donde $b_{i}\in\mathbb{F}$  así como $A_{ij}\in \mathbb{F}$ para todo $1\leq i\leq m$ y $1\leq j\leq n$. Al conjunto de ecuaciones expresadas en \@ref(eq=sistemalineal) se le llama *sistema de $m$ ecuaciones lineales con $n$ incognitas*. A los elementos $A_{ij}$ se les conoce como *coeficientes* del sistema de ecuaciones, siendo espesíficamente el coeficiente de la $i$-ésima fila y la $j$-ésima columna. Una *solución* del sistema es una $n$-tupla $(x_{1},x_{2},\cdots,x_{n})$ (un vector del espacio $\mathbb{R}^{n}$) que satisfaga las ecuaciones \@ref(eq=sistemalineal). Cuando $b_{1}=b_{2}=\cdots b_{m}=0$ se dice que el *sistema de ecuaciones es homogéneo* (cada ecuación es homogénea).

Una forma de resolver un sistema de ecuaciones es con la técnica de eliminación de incógnitas, el cual consiste en multiplicar algunas de las ecuaciones por un escalar de forma que al sumar las ecuaciones se elimine algunas de las incógnitas. Veamos esto con un ejemplo.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-1"><strong>(\#exm:unnamed-chunk-1) </strong></span>	Dado el siguiente sistema homogéneo, sobre el cuerpo de los números reales $\mathbb{R}$
	\begin{eqnarray*}
	\begin{array}{cc}
		x_{1}-4x_{2}+x_{3}&=0\\
		3x_{1}-11x_{2}+2x_{3}&=0
	\end{array}
	\end{eqnarray*}
	Multiplicamos la primera ecuación por el escalar $-3$ y la sumamos a la segunda ecuación, para obtener $-3(x_{1}-4x_{2}+x_{3})+(3x_{1}-11x_{2}+2x_{3})=0$, lo que queda como la siguiente $-3x_{1}+12x_{2}-3x_{3}+3x_{1}-11x_{2}+2x_{3}=0$, sumando términos independientes, obtenemos $x_{2}-x_{3}=0$ por lo tanto $x_{2}=x_{3}$. Ahora, multiplicando por $-2$ la primera ecuación y sumándola a la segunda, se obtiene $-2(x_{1}-4x_{2}+x_{3})+(3x_{1}-11x_{2}+2x_{3})=0$ lo que equivale a $-2x_{1}+8x_{2}-2x_{3}+3x_{1}-11x_{2}+2x_{3}=0$ al sumar los términos semejantes se obtiene que $x_{1}-3x_{2}=0$ por lo que $x_{1}=3x_{2}$. Luego cualquier vector de la forma $(3\lambda,\lambda,\lambda)$ con $\lambda\in\mathbb{R}$ es una solución del sistema homogéneo.
</div>\EndKnitrBlock{example}

En general, este método para resolver un sistema de ecuaciones como \@ref(eq=sistemalineal) consiste en multiplicar por $m$ escalares $c_{1}, c_{2},\cdots ,c_{m}$ cada ecuación del sistema y sumarlas entre si para obtener una *combinación lineal* de las ecuaciones:
\begin{equation}
\begin{array}{ccccccc}
&c_{1}(A_{11}x_{1}&+&\cdots &+&A_{1n}x_{n})=&c_{1}b_{1}\\
&c_{2}(A_{21}x_{1}&+&\cdots &+&A_{2n}x_{n})=&c_{2}b_{2}\\
+&\vdots& &\ddots& &\vdots& \vdots	\\
&c_{m}(A_{m1}x_{1}&+&\cdots &+&A_{mn}x_{n})=&c_{m}b_{m}\\
\cline{2-7}
&(c_{1}A_{11}+\cdots+c_{m}A_{m1})x_{1}&+&\cdots&+&(c_{1}A_{1n}+\cdots +c_{m}A_{mn})x_{n}&=c_{1}b_{1}+\cdots+c_{m}b_{m}
\end{array}
\end{equation}

Es claro que cualquier solución del sistema \@ref(eq=sistemalineal) es solución de la combinación lineal antes descrita.
Ahora bien, si formamos un sistema de $k$ ecuaciones lineales en las que cada una de ellas es una combinación lineal de las $m$ ecuaciones del sistema original, como sigue:
\begin{equation*}
\begin{array}{ccccc}
B_{11}x_{1}+&B_{12}x_{2}+&\cdots +&B_{1n}x_{n}=&d_{1}\\
B_{21}x_{1}+&B_{22}x_{2}+&\cdots +&B_{2n}x_{n}=&d_{2}\\
\vdots& &\ddots& \vdots& \vdots	\\
B_{k1}x_{1}+&B_{k2}x_{2}+&\cdots +&B_{kn}x_{n}=&d_{k}
\end{array}
\end{equation*}\label{sistema2}

se tiene que $(x_{1},x_{2},\cdots, x_{n})$ es solución de \@ref(eq=sistema2) si lo es del sistema \@ref(eq=sistemalineal). Lo contrario no es necesariamente cierto, sin embargo si las ecuaciones de \@ref(eq=sistemalineal) son combinación lineal de las ecuaciones \@ref(eq=sistema2) entonces podemos estar seguros que toda solución del sistema \@ref(eq=sistema2) es también solución de \@ref(eq=sistemalineal). En este caso diremos que *son sistemas de ecuaciones equivalentes*. Y la observación podemos señalarla así:

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-2"><strong>(\#thm:unnamed-chunk-2) </strong></span>	Sistemas de ecuaciones lineales equivalentes tienen exactamente las mismas soluciones.</div>\EndKnitrBlock{theorem}

Lo anterior nos permite buscar las soluciones de cualquier sistema de ecuaciones lineales, buscando un sistema equivalente que sea mas fácil de resolver (por excelencia, trivial). Este método lo explicaremos en la siguiente sección.

## Matrices

En la sección anterior vimos que cuando realizamos combinaciones lineales de ecuaciones lineales, lo que importa son los coeficientes de las ecuaciones originales, siendo las incógnitas prescindibles. Esto nos permite trabajar directamente con los coeficientes para hallar un nuevo sistema lineal equivalente mas sencillo. Por esta razón arreglaremos tales coeficientes en forma rectángular para trabajar con ellos de forma directa. Estos objetos se llaman *matrices*. En la primera parte de esta sección se dará una definición formal y mas general de estos objetos, se definiran algunas operaciones con estos objetos. Para luego volver al problema original, la resolución de sistemas de ecuaciones lineales.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-3"><strong>(\#def:unnamed-chunk-3) </strong></span>	Para enteros positivos $m$ y $n$, *una matriz $m\times n$ sobre el cuerpo $\mathbb{F}$* es una función $A$ del conjunto de los pares $(i,j)\in\{1,2,\cdots m\}\times\{1,2,\cdots n\}$ en el cuerpo $\mathbb{F}$. El *orden de la matriz $A$* es $m\times n$. Los *elementos de la matriz $A$* son los escalares $A(i,j)=a_{ij}$. Suele representarse como un arreglo rectángular de $m$ filas y $n$ columnas, donde el elemento $a_{ij}$ ocupa el puesto en la fila $i$ y la columna $j$ del arreglo, como sigue 
	\begin{equation*}
		\left[ \begin{array}{cccc}
		a_{11}&a_{12}&\cdots &a_{1n}\\
		a_{21}&a_{22}&\cdots &a_{2n}\\
		\vdots& \ddots& \vdots& \vdots\\
		a_{m1}&a_{m2}&\cdots &a_{mn}
		\end{array}\right] 
	\end{equation*}
	La *$i$-ésima fila de la matriz $A$* es el arreglo $A_{i*}=[a_{i1}\; a_{i2}\;\cdots\; a_{in}]$ (puede entenderse como un vector de $\mathbb{R}^{n}$) y la \textit{$j$-ésima columna de la matriz $A$} es el arreglo $A_{*j}=\left[ \begin{array}{c}a_{1j}\\ 
	a_{2j}\\
	\vdots\\
	a_{mj}
	\end{array}\right]$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-4"><strong>(\#def:unnamed-chunk-4) </strong></span>	Dadas las matrices $A$ y $B$ de orden $n\times m$, sobre el cuerpo $\mathbb{F}$, *la suma de las matrices $A$ y $B$*, es la matriz $A+B$ formada por los elementos $(a+b)_{ij}=a_{ij}+b_{ij}$ (la función suma $(A+B)(i,j)=A(i,j)+B(i,j)$). También se puede expresar como:
	\begin{equation*}
		\left[ \begin{array}{cccc}
			a_{11} & a_{12} & \cdots & a_{1n}\\
			a_{21} & a_{22} & \cdots & a_{2n}\\
			\vdots & \vdots & \ddots & \vdots\\
			a_{m1} & a_{m2} & \cdots & a_{mn}\\
		\end{array}\right]+
		\left[ \begin{array}{cccc}
		b_{11} & b_{12} & \cdots & b_{1n}\\
		b_{21} & b_{22} & \cdots & b_{2n}\\
		\vdots & \vdots & \ddots & \vdots\\
		b_{m1} & b_{m2} & \cdots & b_{mn}\\
		\end{array}\right]=
		\left[ \begin{array}{cccc}
		a_{11} + b_{11}& a_{12} + b_{12}& \cdots & a_{1n}+ b_{1n}\\
		a_{21} + b_{21} & a_{22} + b_{22} & \cdots & a_{2n} + b_{2n}\\
		\vdots & \vdots & \ddots & \vdots\\
		a_{m1} + b_{m1} & a_{m2} + b_{m2} & \cdots & a_{mn} + b_{mn}\\
		\end{array}\right]
	\end{equation*}
</div>\EndKnitrBlock{definition}

## Ecuaciones lineales y matrices

Dado un sistema de ecuaciones lineales como \@ref(eq=sistemalineal)
\begin{equation}
\begin{array}{ccccc}
A_{11}x_{1}+&A_{12}x_{2}+&\cdots +&A_{1n}x_{n}=&b_{1}\\
A_{21}x_{1}+&A_{22}x_{2}+&\cdots +&A_{2n}x_{n}=&b_{2}\\
\vdots& &\ddots& \vdots& \vdots	\\
A_{m1}x_{1}+&A_{m2}x_{2}+&\cdots +&A_{mn}x_{n}=&b_{m}
\end{array}
\end{equation}
Podemos representar este sistema de ecuaciones como un sistema matricial $AX=B$, donde $A$ es la matriz de los coeficientes del sistema de ecuaciones, $X$ es una matriz de incógnitas y $B$ una matriz de términos independientes de la siguiente forma:
\begin{equation}
	\left[ \begin{array}{cccc}
		A_{11}&A_{12}&\cdots &A_{1n}\\
		A_{21}&A_{22}&\cdots &A_{2n}\\
		\vdots& \ddots& \vdots& \vdots\\
		A_{m1}&A_{m2}&\cdots &A_{mn}
	\end{array}\right] 
	\cdot
	\left[ \begin{array}{c}
		x_{1}\\
		x_{2}\\
		\vdots\\
		x_{n}
	\end{array}\right] =
	\left[ \begin{array}{c}
		b_{1}\\
		b_{2}\\
		\vdots\\
		b_{n}
	\end{array}\right] 
\end{equation}