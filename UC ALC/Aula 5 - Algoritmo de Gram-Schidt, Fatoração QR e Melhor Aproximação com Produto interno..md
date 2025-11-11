
 23/10/24
 Algoritmo de Gram-Schmidt

![[Pasted image 20241023114903.png]]
Boyd Vanderberghe pg. 192


![[Pasted image 20241023122341.png]]

![[Pasted image 20241023122439.png]]
Boyd Vanderberghe pg 182


**Teorema de Pitágoras**
Sejam $p$ e $q$ vetores ortogonais então $\|p+q\|^2 = \|p\|^2 + \|q\|^2$.

_Demonstração:_ $\| p+q\|^2 = \langle p+q,\, p+q \rangle = \|p\|^2 + \langle p,\, q \rangle+ \langle q,\, p \rangle = \|q\|^2$.


**Teorema: Melhor aproximação com produto interno.**
Considere um espaço vetorial com um produto interno. Sejam $u_1,u_2,\ldots,u_k$ vetores ortonormais e $U$ o espaço gerado por eles. Dado $v$, o vetor de $U$ que tem a menor distância a $v$ é a projeção ortonormal de $v$ sobre $U$.
Isto é, $$ \|v-p\| \leq \|v-u\| \quad \text{para qualquer } u\in \text{span}[u_1,\ldots,u_n] $$para 
$$ p = \langle v,\ u_1 \rangle\, u_1 +  \langle v,\ u_2 \rangle\, u_2 + \ldots + \langle v,\ u_n \rangle \, u_n.$$

_Demonstração:_ Como $v-u$ é ortogonal a $p-u \in U$ (resultado anterior) então pelo Teorema de Pitágoras, 
$\|v-u\|^2 = \|v-p+p-u\|^2 = \|v-p\|^2 + \|p-u\|^2$.
Daí, $\| v-p\|^2 \leq \|v-p\|^2 + \|p-u\|^2 = \|v-u\|^2$.


Exemplo:
Polinômios e produto interno com avaliação dos polinômios. Minimos quadrados.

---
