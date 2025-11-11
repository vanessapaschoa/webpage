
Fonte: https://en.wikipedia.org/wiki/Conjugate_gradient_method

We say that two non-zero vectors **u** and **v** are conjugate (with respect to A if $\displaystyle \mathbf {u} ^{\mathsf {T}}\mathbf {A} \mathbf {v} =0$

Since A is symmetric and positive-definite, the left-hand side defines an inner product 
$\displaystyle \mathbf {u}^{\mathsf {T}}\mathbf {A} \mathbf {v} =\langle \mathbf {u} \mathbf {v} \rangle _{\mathbf {A} }:=\langle \mathbf {A} \mathbf {u} ,\mathbf {v} \rangle =\langle \mathbf {u} ,\mathbf {A} ^{\mathsf {T}}\mathbf {v} \rangle =\langle \mathbf {u} ,\mathbf {A} \mathbf {v} \rangle$


Suppose that P={p1,…,pn} is a set of n![{\displaystyle n}](https://wikimedia.org/api/rest_v1/media/math/render/svg/a601995d55609f2d9f5e233e36fbe9ea26011b3b) mutually conjugate vectors with respect to A![{\displaystyle \mathbf {A} }](https://wikimedia.org/api/rest_v1/media/math/render/svg/0795cc96c75d81520a120482662b90f024c9a1a1), i.e. piTApj=0![{\displaystyle \mathbf {p} _{i}^{\mathsf {T}}\mathbf {A} \mathbf {p} _{j}=0}](https://wikimedia.org/api/rest_v1/media/math/render/svg/15bc60ca4ebe3169413624c583d818f8f3160501) for all i≠j![{\displaystyle i\neq j}](https://wikimedia.org/api/rest_v1/media/math/render/svg/d95aeb406bb427ac96806bc00c30c91d31b858be)
we may express the solution x∗ of Ax=b in this basis:

$$\displaystyle \mathbf {x} _{*}=\sum _{i=1}^{n}\alpha _{i}\mathbf {p} _{i}\Rightarrow \mathbf {A} \mathbf {x} _{*}=\sum _{i=1}^{n}\alpha _{i}\mathbf {A} \mathbf {p} _{i}$$

Left-multiplying the problem Ax=b![{\displaystyle \mathbf {Ax} =\mathbf {b} }](https://wikimedia.org/api/rest_v1/media/math/render/svg/e68388b7df59f536a3bef4e70def2f2bb36f48c0) with the vector pkT![{\displaystyle \mathbf {p} _{k}^{\mathsf {T}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/d4abb42f156425321819c42e7b4e35a1fb61541e) yields

pkTb=pkTAx∗=∑i=1nαipkTApi=∑i=1nαi⟨pk,pi⟩A=αk⟨pk,pk⟩A![{\displaystyle \mathbf {p} _{k}^{\mathsf {T}}\mathbf {b} =\mathbf {p} _{k}^{\mathsf {T}}\mathbf {A} \mathbf {x} _{*}=\sum _{i=1}^{n}\alpha _{i}\mathbf {p} _{k}^{\mathsf {T}}\mathbf {A} \mathbf {p} _{i}=\sum _{i=1}^{n}\alpha _{i}\left\langle \mathbf {p} _{k},\mathbf {p} _{i}\right\rangle _{\mathbf {A} }=\alpha _{k}\left\langle \mathbf {p} _{k},\mathbf {p} _{k}\right\rangle _{\mathbf {A} }}](https://wikimedia.org/api/rest_v1/media/math/render/svg/85d909060186a1758446ec9895eac8b55367fb19)

and so

αk=⟨pk,b⟩⟨pk,pk⟩A.![{\displaystyle \alpha _{k}={\frac {\langle \mathbf {p} _{k},\mathbf {b} \rangle }{\langle \mathbf {p} _{k},\mathbf {p} _{k}\rangle _{\mathbf {A} }}}.}](https://wikimedia.org/api/rest_v1/media/math/render/svg/2dfd69512621e6a872d9df9c59efa3e580a72020)



![[Anexos/Pasted image 20241118114241.png]]


Gradiente Conjugado