
A decomp SVD é uma ferramenta muito potente na resolução de problemas que envolvem uma matriz. O problema no entanto é que obter a decomposição SVD depende de encontrar os autovalores de A^T A

___
# Como é calculado a SVD - ChatGPD:
A decomposição SVD (Singular Value Decomposition) de uma matriz é feita usando algoritmos numéricos que envolvem **autovalores**, **transformações ortogonais** e **redução de matriz**.

Dada uma matriz$A \in \mathbb{R}^{m \times n}$, queremos encontrar:
$$
A = U \Sigma V^T
$$
- $U \in \mathbb{R}^{m \times m}$ matriz ortogonal (ou unitária).
- $\Sigma \in \mathbb{R}^{m \times n}$ matriz diagonal com valores singulares.
- $V \in \mathbb{R}^{n \times n}$ matriz ortogonal.
___
## 🧠 Etapas principais do algoritmo

### 1. Redução Bidiagonal

- A matriz $A$ é transformada numa matriz **bidiagonal** $B$, usando:
  - **Reflexões de Householder** ou
  - **Rotações de Givens**.
- Isso reduz o custo computacional e melhora a estabilidade numérica.

___
### 2. Cálculo da SVD da matriz bidiagonal

Usa-se o **algoritmo QR iterativo**:

- Aplica fatorações QR repetidas em$B$.
- Evita formar$A^T A$explicitamente (para não perder precisão).
- Converge para os **valores singulares**$\sigma_1 \ge \sigma_2 \ge \dots \ge 0$.
___
##### 3. Construção de$U$,$\Sigma$,$V$

- Vetores singulares à esquerda (colunas de$U$) vêm de$AA^T$.
- Vetores singulares à direita (colunas de$V$) vêm de$A^T A$.

> **Importante**: Não se calcula$AA^T$ou$A^T A$diretamente — os vetores são obtidos através das iterações QR sobre a matriz bidiagonal.

___

###### Algoritmos usados na prática

- **Golub–Kahan SVD** (mais comum)
- **Jacobi SVD** (alta precisão, mas mais lento)
- **Divide and Conquer** (rápido para matrizes grandes)
- **Lanczos SVD** (para matrizes esparsas)

######  Resumo

1. Redução de$A$a forma bidiagonal:$A \to B$
2. Iterações QR sobre$B$
3. Extração de$U$,$\Sigma$,$V$

###### Referências

- Golub, G. H., & Van Loan, C. F. (1996). *Matrix Computations*.
- NumPy / SciPy source code (implementações de `linalg.svd`)







