
 21/10/24
 
 _Faltou na aula passada: Verificação da desig. triangular com uso da desig. de cauchy Schwarz._
---


==Um produto interno definirá a geometria do espaço.==

---
### Produto Interno



![[angulo-prod-interno]]
Da Lei dos Cossenos temos:

$$\|x-y\|^2 = \|x\|^2 + \|y\|^2 + 2 \cos(\alpha) \|x\| \|y\|$$
---

Desta conta temos

$$ \cos(\alpha) = \frac{x_1y_1 + x_2y_2 + \cdots + x_ny_n}{\|x\|\|y\|}= \frac{x^Ty}{ \|x\| \|y\|}$$

$$ x^T y = \cos(\alpha) \| x \| \|y\|$$

Pela desig. de Schwarz
$$-1 \leq \frac{x^T y}{\|x\| \|y\|} \leq 1 $$

Relacionando com a geometria temos
$x^T y >0 \iff 0$ projeção positiva e
$x^T y >0 \iff 0$ projeção negativa.


---
Definindo $x^T y = \langle x,\, y \rangle$
Temos:
- $x^T x = \langle x ,\, x\rangle \geq 0$
- $x^T y = \langle x ,\, y \rangle = \langle y ,\, x\rangle = y^T x$
- $\lambda$
- $x+w, y$

Requerendo estas mesmas propriedades para alguma outra função podemos ter outros produtos internos.

- $\langle x,\, y \rangle = x^T y$ é o produto interno canônico.

Dizemos que uma função de $\mathbb R^n \times \mathbb R^n \to \mathbb R$ define um produto interno em $\mathbb R^n$ quando satisfaz as seguintes propriedades:
- Positividade: $\langle x ,\, x\rangle \geq 0$
- Definição: $\langle x ,\, x\rangle = 0$ apenas para $x=0$
- Simetria: $\langle y ,\, x \rangle = \langle x ,\, y\rangle$
- Linearidade: $\langle\lambda x ,\, y \rangle = \lambda \langle x ,\, y\rangle$ e $\langle x + w,\, y \rangle = \langle x ,\, y \rangle + \langle w,\, y \rangle$
---

Dizemos que uma função de $\mathbb C^n \times \mathbb C^n \to \mathbb C$ define um produto interno em $\mathbb C^n$ quando satisfaz as seguintes propriedades: 
 - Positividade: $\langle x ,\, x\rangle \geq 0$
- Definição: $\langle x ,\, x\rangle = 0$ apenas para $x=0$
- Simetria: $\langle y ,\, x \rangle = \overline{\langle x ,\, y\rangle}$
- Linearidade: $\langle\lambda x ,\, y \rangle = \lambda \langle x ,\, y\rangle$ e $\langle x + w,\, y \rangle = \langle x ,\, y \rangle + \langle w,\, y \rangle$
---

Por exemplo: $\langle x,\, y \rangle = 2 x_1 y_1 + x_2y_2 + \cdots + x_{n-1} y_{n-1} + 2 x_n y_n$

---
- Para saber como funciona o produto interno no espaço basta saber o que acontece entre vetores de uma base.

Na base $e_1, e_2, \ldots, e_n$ temos:
$$ \begin{align} \langle x ,\, y \rangle &= \langle x_1 e_1 + \cdots x_n e_n ,\, y_1 e_1 + \cdots y_n e_n\rangle \\[10pt]
& = x_1 \langle e_1 ,\, y \rangle + \cdots + x_n \langle e_n ,\, y \rangle \\[10pt]
& = x_1 y_1 \langle e_1 ,\, e_1 \rangle + \ldots + x_1y_n \langle e_1 ,\, e_n  \rangle + \cdots + x_n y_1 \langle e_n ,\, e_1 \rangle + \ldots + x_n y_n \langle e_n ,\, e_n  \rangle \\[10pt]
& = [x_1 \ x_2 \ \cdots x_n ] 
	\left[ \begin{array}{cccc}
	 \langle e_1 ,\, e_1 \rangle &  \langle e_1 ,\, e_2 \rangle & \cdots &  \langle e_1 ,\, e_n \rangle \\
	 \vdots & \vdots & \vdots & \vdots \\
	  \langle e_1 ,\, e_1 \rangle &  \langle e_1 ,\, e_2 \rangle & \cdots &  \langle e_1 ,\, e_n \rangle 
	\end{array} \right]
	\left[ \begin{array}{c}
	y_1 \\ y_2 \\ \vdots \\ y_n
	\end{array}\right]\\[10pt]
	= x^T M x
\end{align}
$$

- Um produto interno fica totalmente determinado pela matriz $M$. Nos referiremos a um produto interno diferente do canônico por produto interno $M$.

> [!NOTE] Qual a variedade de produtos internos que temos em $\mathbb R^n$?
###### $M$ define um produto interno se, e somente se, 
$M$ é simétrica e definida positiva.

Exemplo: verificar se a matriz abaixo pode definir um produto interno.
![[Pasted image 20241021101319.png]]


---

Em uma outra base $v_1, v_2, \ldots, v_n$ temos:
$$ \begin{align} \langle x ,\, y \rangle &= \langle x_1' v_1 + \cdots x_n' v_n ,\, y_1' v_1 + \cdots y_n' v_n\rangle \\[10pt]
& = [x_1' \ x_2' \ \cdots x_n' ] 
	\underbrace{\left[ \begin{array}{cccc}
	 \langle v_1 ,\, v_1 \rangle &  \langle v_1 ,\, v_2 \rangle & \cdots &  \langle v_1 ,\, v_n \rangle \\
	 \vdots & \vdots & \vdots & \vdots \\
	  \langle v_1 ,\, v_1 \rangle &  \langle v_1 ,\, v_2 \rangle & \cdots &  \langle v_1 ,\, v_n \rangle 
	\end{array} \right]}_{G}
	\left[ \begin{array}{c}
	y_1' \\ y_2' \\ \vdots \\ y_n'
	\end{array}\right]
\end{align}
$$


**Matriz de Gram de $v_1, v_2, \ldots,v_n$:
$$G = [\langle v_i ,\, v_j \rangle]_{i,j=1}^n$$

**Matriz de Gram de $v_1, v_2, \ldots,v_n$ com produto interno canônico**
$$\left[ \begin{array}{cccc} 
v_1^T v_1 & v_1^Tv_2 & \cdots & v_1^Tv_n \\
\vdots & \vdots & \ddots & \vdots \\
v_n^T v_1 & v_n^Tv_2 & \cdots & v_n^Tv_n \\
\end{array} \right] = 
\left[ \begin{array}{c}
v_1^T  \\ \hline
\ v_2^T \ \\ \hline
 \vdots \\ \hline
v_n^T \end{array} \right] \, [v_1 | v_2 | \ldots | v_n ] = V^TV,
$$

 com $V = [v_1 | v_2 | \ldots | v_n ]$.
 

- $M$ é a matriz de Gram de $e_1,e_2,\ldots,e_2$ com relação a um determinado produto interno. 


Note que 
- $
$ é simétrica/hermitiana
- $x^T G x > 0$ para todo $x\neq 0$  ($G$ é definida positiva) 
- Podemos mostrar que $det(G) \neq 0 \iff$ $v_1, \ldots,v_n$ são $LI$.


**Norma e Produto Interno**

Dado um produto interno temos uma norma definida por
$\| x\| = \sqrt{\langle x,\, x \rangle}$

Dado um produto interno considere a norma definida por $\| x\| = \sqrt{\langle x,\, x \rangle}.$ 
Vale que:
- **Regra do Paralelogramo e Identidade de Polarização:** $$\| x+y\|^2 + \|x-y\|^2 = 2( \|x\|^2 + \| y\|^2)$$
- **Identidade de Polarização:** $$\langle x,\, y \rangle = \frac{\|x+y\|^2-\|x-y\|^2}{4}$$
- Uma norma está relacionada a um produto interno se, e somente se, a regra do paralelogramo é válida e neste caso o produto interno pode ser recuperado pela Identidade de Polarização. Verifique!

Assim, todo produto interno satisfaz
$$ \langle x, \, y \rangle = \frac{1}{2}\left(\|x+y\|^2 -\|x\|^2 -\|y\|^2 \right)$$

#### Ortogonalidade

Dado um produto interno dizemos que dois vetores $x$ e $y$ são ortogonais quando $\langle x, \ y \rangle = 0$.

Um conjunto de vetores é dito ortogonal se os vetores são ortogonais dois a dois.

Um conjunto de vetores é dito ortonormal se além de ortogonais os vetores são unitários (norma igual a um).

- Um conjunto de vetores ortogonais é LI. Verifique. Portanto, $n$ vetores ortogonais formam base em $\mathbb R ^n$.
- Cada produto interno gera diferentes bases ortogonais.


Dado um produto interno $M$ podemos fazer seu cálculo reduzindo-o ao cálculo do produto interno canônico através de uma mudança de base.

- Tome uma fatoração de $M$ do tipo $M = B^TB$ (isso sempre é possível, por exemplo, veremos a fatoração de Cholesky para $M$ simétrica e definida positiva). Então,
$$\langle v, \, w\rangle = v^T M w = v^T (B^T B) w = (Bv)^T (Bw)$$


Obs.: ![[Pasted image 20241025070139.png|400]]

Então o cálculo do produto interno $M$ correspondente ao cálculo do produto interno canônico fazendo a mudança de base com $B$.

- Toda base ortogonal no produto interno canônico corresponde a uma base ortogonal do produto interno $M$ pela transformação $B$ (matriz de mudança de base):

$$ q_1, \ldots, q_n \ \text{ com }\  q_i^Tq_j=0 \iff B^{-1}q_1, \ldots, B^{-1}q_n \ \text{ com }\ (B^{-1}q_i)^TM(B^{-1}q_j)=0$$

- Por outro lado, admitindo que uma base $v_1,v_2,\ldots,v_n$ é ortonormal com $M$ podemos recuperar $M$ considerando $V=[v_1 \, v_2 \, \cdots \, v_n]$ e sua inversa $V^{-1}$ então $M = (V^{-1})^T V^{-1}$. De fato, $$\begin{align} V^T M V &= I\\
(V^{-1})^T V^T M V V^{-1} &= (V^{-1})^T V^{-1}\\
M &= (V^{-1})^T V^{-1} \end{align}$$


---
#### Projeção

Dizemos que $p$ é a projeção ortogonal de $v$ em um subespaço $U$ quando $v-p$ é ortogonal é qualquer vetor de $U$.

![[projecao]]

**Teorema:** Sejam $u_1,u_2,\ldots,u_k$ vetores ortonormais e $U$ o espaço gerado por eles. Então a projeção de $v$ sobre $U$ é
$$ \langle v,\ u_1 \rangle\, u_1 +  \langle v,\ u_2 \rangle\, u_2 + \ldots + \langle v,\ u_n \rangle \, u_n$$

_Demonstração:_
Sendo $p = \langle v,\ u_1 \rangle u_1 +  \langle v,\ u_2 \rangle u_2 + \ldots + \langle v,\ u_n \rangle u_n$ então $\langle p,\, u_i \rangle =  \langle v,\, u_i \rangle$.
Daí,
	$$\langle v-p, u_i \rangle  = \langle v, u_i \rangle - \langle p, u_i \rangle = 0$$
E por ortogonal a qualquer vetor da base será ortogonal a qualquer vetor de $U$.

- A projeção de $v$ sobre $U$ pode ser reescrita como 
$$\begin{align} & \langle v,\ u_1 \rangle\, u_1 +  \langle v,\ u_2 \rangle\, u_2 + \ldots + \langle v,\ u_n \rangle \, u_n \\[10pt]
& \langle u_1,\ v \rangle\, u_1 +  \langle u_2,\ v \rangle\, u_2 + \ldots + \langle u_n,\ v \rangle \, u_n \\[10pt]
& u_1^T M v\, u_1  + u_2^T M v\, u_2 + \cdots + u_n^T M v\, u_n \\[10pt] 
& u_1\, u_1^T M v  + u_2 \, u_2^T M v + \cdots + u_n \, u_n^T M v \\[10pt] 
& (u_1 u_1^T + u_2u_2^T + \cdots + u_nu_n^T)Mv 
\end{align}$$
Como $M = (U^{-1})^T U^{-1}$ chegamos em
$$[u_1 \ u_2 \ \cdots \ u_k \ 0 \ \cdots \ 0  ] U^{-1} v$$
(Para encontrar $U^{-1}$ é interessante calcular a decomposição $QR$)

---


Podemos gerar a partir de uma base inicial uma base ortogonal pelo processo de ortogonalização de Gram-Schimidt.

