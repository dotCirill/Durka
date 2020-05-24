---
title: Глава 1
---

## Собственные числа и собственные вектора оператора. Матрица оператора в базисе из собственных векторов.

<h2 class="stitle" id="t_64_2">Теорема 64.2</h2>
Пусть $\mathcal{A}$ - ЛО в ЛП $L$. Число $\lambda \in \mathbb{C}$ и $x \in L \ne \textbf{0}$ - собственное число и соответствующий этому числу собственный вектор, если $\mathcal{A}x=\lambda x$

<span class="stitle"> Доказательство: </span> 

1. $\mathcal{A}x=\lambda x = y \iff AX=\lambda X = Y$
2. Матрицы одного оператора $\mathcal{A}$ в разных базисах связаны соотношением $A'=C^{-1}AC$, следовательно они подобны и их характеристические многочлены совпадают.
3. $\lambda$ - собственное число $\iff \lambda$ - корень $\phi_{\mathcal{A}}(t)$



<h2 class="stitle">Лемма</h2>
Матрица $A$ ЛО $\mathcal{A}$ в базисе $e$ имеет диагональный вид $\iff$ базис $e$ состоит из собственных векторов от $\mathcal{A}$, при этом на диагонали стоят собственные числа.

<span class="stitle"> Доказательство: </span> 

$e_j$ - собственный вектор
$\iff \mathcal{A}e_j = \lambda e_j \xrightarrow{e} 
    \left(
    \begin{array}{c}
        0 \\
        \vdots \\
        \lambda \\
        \vdots \\
        0
    \end{array}
    \right)
    \begin{array}{c}
         \\
         \\
        (j) \\
         \\
         \\
    \end{array} \iff A_{*j} = 
    \left(
    \begin{array}{c}
        0 \\
        \vdots \\
        \lambda \\
        \vdots \\
        0 \\
    \end{array}
    \right)
    \begin{array}{c}
         \\
         \\
        (j) \\
         \\
         \\
    \end{array} \iff A = \text{diag}(\lambda \ldots \lambda)$