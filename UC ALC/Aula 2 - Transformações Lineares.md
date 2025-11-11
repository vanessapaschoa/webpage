10/10/24

	[Aula 2 prof. Luis Felipe](https://drive.google.com/open?id=1Gd_4TiF2tDPc8Mlbn1w4ioHFrUIrG729&usp=drive_fs)




**Transformações Lineares**
- São as funções mais elementares
- Satisfazem
	(I)     $f(\alpha x) = \alpha f(x)$ (Proporção/Regra de três)
	e
	(II)	$f(x+w)=f(x)+f(w)$ (Aditividade)

que podem ser reescritas como
	$f(\alpha x+z) = \alpha f(x) + f(z)$


_Exemplo:_ um certo comprimido tem em um miligrama $m_1$ mg de um componente, $m_2$  mg de outro, $m_3$ mg de outro, e um segundo comprimido tem em um miligrama $k_1$ do primeiro componente, $k_2$ do outro e $k_3$ do outro.

Podemos organizar da seguinte forma: 
Sejam $x_1$ e $x_2$, em miligramas, a quantidade tomada de cada comprimido. Então temos o seguinte resultado
$$f(1,0) = (m_1,m_2,m_3)$$
$$f(0,1) = (k_1,k_2,k_3)$$
$$f(x_1,x_2) = f((x_1,0)+(0,y_1)) = f(x_1,0) + f(0,x_2) $$
$$= f(x_1(1,0)) + f(x_2(0,1))= x_1f(1,0)+y_1f(0,1) $$
$$= x_1(m_1,m_2,m_3) + y_1(k_1,k_2,k_3)$$
Note que esta é um função linear.

- Das propriedade decorre que $f(0)=0$
- Se $f:\mathbb R \to \mathbb R$ basta (I) ou (II) mais continuidade ou monotonicidade (procure por _Cauchy's function_).


Transformações Lineares - Matriz

Considere em $\mathbb{R}^n$
$e_1 = (1,0,0, \ldots, 0,0)$



a base canônica


Seja $T$ uma transformação linear de $\mathbb{R}^n$ para $\mathbb{R}^m$
Aplicando $T$ nos vetores da base temos 

$z_1 = T(e_1)$
$z_2 = T(e_2)$
...
$z_n = T(e_n)$


Então, para um vetor $x$ qualquer de $\mathbb{R}^n$ temos

$x = x_1 e_1 + x_2 e_2 + \cdots + x_n e_n$

e pelas propriedades de linearidade da Transformação Linear

$T(x) = x_1 T(e_1) + x_2 T(e_2) + \cdots + x_n T(e_n)$

Escrevendo com a notação de vetor coluna

Matriz de T:

Im(A)
Nu(A)

- Im(A) e Nu(A) são espaços vetoriais


**Multiplicação de Matriz por coluna**
**Multiplicação de matrizes** <-> Combinação/Composição de Transf. Lineares












	 
 