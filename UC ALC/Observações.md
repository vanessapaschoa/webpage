 #ALC

#### Algoritmo para completar a base ortogonal
Ideia: Piero Andreeto
Seja Q a matriz de reflexão ortogonal sobre $(span\{q_1, q_2, \ldots, q_r\})^\perp$ sendo $q_1, q_2, \ldots, q_r$ ortonormais.
Então $$ Q = I - 2 (q_1q_1^* + \cdots + q_rq_r^*) $$

Dado $v$ considere a matriz de reflexão ortogonal que leva $v_1 = v/\|v\|$ em $e_1$. Esta matriz faz uma reflexão sobre $\textcolor{green}{(span\{u\})^\perp}$ com  $u =(v_1-e_1)/\|v_1-e_1\|$. Essa matriz é
$$Q= I - 2uu^*$$
![[Drawing 2024-10-25 19.42.16.excalidraw]]

A matriz $Q= I - 2uu^*$ ==é ortogonal/unitária com a primeira coluna sendo $v$ e as demais colunas portanto ortogonais a $v$, gerando portanto vetores que completam a base que contém o vetor $v$==.
- Ortogonal/unitária: $$QQ^* = (I-2uu^*)(I - 2uu^*) = I - 4uu^* + 4 uu^*uu^* = I$$
- Primeira coluna de Q é $v$: $$ Qe_1 = I - 2q_1q_1^* e_1 = I - 2 ((v-e_1)v^Te_1 -1)/\|v-e_1\|$$ 


_ChatGPT 10/02/2025_
A teoria dos **espaços de Krylov** é fundamental na álgebra linear numérica, especialmente em métodos iterativos para resolver sistemas lineares e problemas de autovalores. Os resultados mais importantes dessa teoria incluem:

1. **Definição do Espaço de Krylov**:  
    Dado um operador linear A∈Rn×nA \in \mathbb{R}^{n \times n} e um vetor bb, o espaço de Krylov de ordem kk é definido como:
    
    Kk(A,b)=span{b,Ab,A2b,…,Ak−1b}\mathcal{K}_k(A, b) = \text{span} \{ b, Ab, A^2b, \dots, A^{k-1}b \}
    
    Esse espaço contém informações essenciais sobre o comportamento da matriz AA, incluindo suas iterações sobre bb.
    
2. **Métodos Iterativos para Sistemas Lineares**:  
    Os espaços de Krylov são a base para algoritmos como:
    
    - **Gradientes Conjugados (CG)** para matrizes simétricas e definidas positivas.
    - **GMRES (Generalized Minimal Residual Method)** para matrizes não simétricas.
    - **BiCGSTAB (Bi-Conjugate Gradient Stabilized Method)** como uma alternativa ao GMRES.
3. **Métodos de Aproximação de Autovalores**:
    
    - **Método de Arnoldi**: Gera uma base ortonormal do espaço de Krylov e leva ao algoritmo **Lanczos**, que é eficiente para matrizes simétricas.
    - **Transformação de Hessenberg e Tridiagonalização**: Usadas em métodos como QR iterativo.
4. **Teorema de Optimalidade de Krylov**:  
    Muitos métodos iterativos baseados em espaços de Krylov são ótimos dentro da subespaço gerado. Por exemplo, o método dos gradientes conjugados minimiza o erro na norma AA-energia dentro de Kk(A,b)\mathcal{K}_k(A, b).
    
5. **Redução de Ordem de Modelo (MOR)**:
    
    - Espaços de Krylov são usados na construção de aproximações de sistemas dinâmicos de alta dimensão, como em métodos de redução de modelo via Padé.
6. **Interpolação de Polinômios de Krylov**:
    
    - A teoria ajuda na construção de polinômios minimizadores que aproximam f(A)bf(A)b para funções matriciais como a exponencial de matriz.

Em resumo, a teoria de Krylov fornece a base matemática para resolver grandes sistemas de equações lineares e encontrar autovalores dominantes de maneira eficiente, sendo essencial na computação científica e na simulação numérica.
