15/10/24

Nu(A) = 

Nu(A) = {0} equivale aos vetores coluna de A serem LI.

#### Teorema do Núcleo e Imagem
Seja $A \in \mathbb{R}^{m\times n}$ então $dim(Im(A)) + dim(Nu(A)) = n.$

_Demonstração:_
	Seja $(v_1, v_2, \ldots, v_k)$ base de $Nu(A)$.
	Complete a base do espaço: $(v_1, v_2, \ldots, v_k, v_{k+1}, \ldots, v_n)$.
	Qualquer vetor de $Im(A)$ é da forma $Ax$. 
	Por sua vez, $x = x_1 v_1 + \ldots +x_k v_k+ x_{k+1}v_{k+1} + \ldots + x_n v_n$.
	Daí, $Ax = x_{k+1}Av_{k+1} + \ldots + x_n Av_n$.
	Portanto, $Av_{k+1},\ldots, Av_n$ geram $Im(A)$.
	Além disso, são LI pois
	  $\alpha_{k+1}Av_{k+1} + \cdots + \alpha_n Av_n = 0$
	implica 
	  $A(\alpha_{k+1}v_{k+1}+ \cdots +\alpha_n v_n)$ = 0
	O que implica que 	$\alpha_{k+1}v_{k+1}+ \cdots +\alpha_n v_n$ está no $Nu(A)$ e assim
	  $\alpha_{k+1}v_{k+1}+ \cdots +\alpha_n v_n = \beta_1\, v_1 + \cdots + \beta_k\, v_k$.
	Ou seja, 
	  $0 = \beta_1\, v_1 + \cdots + \beta_k \, v_k - \alpha_{k+1}v_{k+1}- \cdots -\alpha_n v_n$
	  Mas como estes vetores são LI então todos os coeficientes são nulos. Em particular os $\alpha's$ nulos implicam que  $Av_{k+1},\ldots, Av_n$ são LI.
	Portanto, $Av_{k+1},\ldots, Av_n$ é base de $Im(A)$ e assim temos que a dimensão de $Im(A)$ é $n-k$.
###### %%Demonstração começando pelo espaço imagem (mais longa...)%%

%%Dada uma matriz $A \in \mathbb{R}^{m\times n}$ seja $k$ o número máximo de colunas LI de $A$. Assim, a dimensão de $Im(A)$ é $k$. Seja $A = B\ C$.
onde $B \in \mathbb{R}^{m\times k}$ contém $k$ colunas LI de $A$ e $C \in \in \mathbb{R}^{k\times n}$ é de tal forma a recuperar $A$.
Podemos reorganizar $A$ e $C$ usando uma matriz de permutação $P$ tal que  $C P  = [ \ I_k \ | \ D \ ]$
E como $P P^T = I_n$ 
$$ \begin{array}{rcl} 
A \ P ^T & = &  B \ [ \ I_k \ | \ D \ ] \\
\ & = & B\ [ I_k \ | d_1 | d_2 | \cdots | d_{n-k}]
\end{array} $$
Os vetores 
$$
e_1, e_2, \ldots, e_k, \left[ \begin{array}{r} d_1 \\ \hline -1 \\ 0 \\ \vdots \\ 0 \end{array} \right], 
\left[ \begin{array}{r} d_2 \\ \hline 0 \\ -1 \\ \vdots \\ 0 \end{array} \right], 
\ \ldots,
\left[ \begin{array}{r} d_{n-k} \\ \hline 0 \\ 0 \\ \vdots \\ -1 \end{array} \right]
$$
formam uma base de $\mathbb{R}^n$.
Note que $AP^T e_1,\ AP^T e_2, \ \ldots, A P^T e_k$  geram a Im(A)
e os demais tais que multiplicados por $A$ a direita resultam no vetor nulo.
Além disso, qualquer vetor de Nu(A) pode ser gerado por estes ultimos (mostrar)

Sem matrizes: considerar uma base de Im(A), pegar os correspondentes vetores em Rn, verificar que eles são LI, acrescentar vetores a estes de forma a obter uma base de Rn. Cada um destes que foram acrescentados, aplicados A podem ser escritos como combinacao da base de Im(A). Pegar estes coeficientes e trocar a base pelos primeiros acrescidos dos ultimos subtraidos da combinação linear correspondente sem A. %%

#### Transformação Sobrejetora/Injetora

- Sobrejetora equivale a $Im(A) = \mathbb{R}^m$. Ou seja, uma transformação linear sobrejetora equivale a matriz $A$ ter colunas que gerem $\mathbb R ^m$.  Condição necessária: o número de colunas é $n$ e tal que $n\geq m$ (matriz horizontal).
- Injetora equivale a não ter dois vetores com mesma imagem, que por sua vez, equivale ao $Nu(A)=\{0\}$. Por sua vez, isto equivale aos vetores coluna de $A$ serem LI. Isto só pode ocorrer se a dimensão do núcleo for zero e portanto a dimensão da imagem for $n$. Condição necessária: imagem com dimensão $n$ contida em $\mathbb R^m$ implica que $n \leq m$ (matriz vertical)
- Para que a transformação seja bijetora temos necessariamente que $n=m$. Além disso, note que nesse caso, basta que a transf. linear seja sobrejetora ou injetora para que seja bijetora.


%% colocar aqui o teorema $Im(A^T) + Nu(A) = R^n$ que esta na Aula 6 %%

#### Inversa
##### Inversa a esquerda

##### Inversa a direita


#### Norma

- $\| x\|_2 = \sqrt{x_1^2 + x_2^2 + \cdots + x_n^2}$
- $\| x\| _1 = |x_1| + |x_2| + \cdots + |x_n|$
- $\|x\|_\infty$
 





![[Pasted image 20241015141939.png]]

![[Pasted image 20241015142008.png]]
 
