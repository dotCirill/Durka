---
title: Глава 1
---

## Собственные числа и собственные вектора оператора. Матрица оператора в базисе из собственных векторов.

### Теорема 64.2
Пусть $\mathcal{A}$ - ЛО в ЛП $L$. Число $\lambda \in \mathbb{C}$ и $x \in L \ne \textbf{0}$ - собственное число и соответствующий этому числу собственный вектор, если $\mathcal{A}x=\lambda x$

<span class="stitle"> Доказательство: </span> 

1. $\mathcal{A}x=\lambda x = y \iff AX=\lambda X = Y$
2. Матрицы одного оператора $\mathcal{A}$ в разных базисах связаны соотношением $A'=C^{-1}AC$, следовательно они подобны и их характеристические многочлены совпадают.
3. $\lambda$ - собственное число $\iff \lambda$ - корень $\phi_{\mathcal{A}}(t)$



### Лемма
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


## Евклидовы и унитарные пространства. Процесс ортогонализации Грама-Шмидта
<span class="stitle"> Определение: </span>

ЛП под полем $\mathbb{R}$ с введенным в нем скалярном произведением называется евклидовым (над полем $\mathbb{C}$ - унитарным). 

<span class="stitle"> Замечание: </span>

В унитарном пространстве свойство симметрии скалярного произведения заменяется на $(x,y) = \overline{(y, x)}$. Остальные свойства остаются прежними (положительная определенность, линейность по первому аргументу). Скалярное произведение для столбцов имеет вид: $(X, Y) = \sum x_i \cdot \overline{y_i} = X^T\overline{Y}$. Выполнение свойств можно проверить.

### Теорема

Пусть $\mathcal{E}$ - евклидово пространство
    
1. $(x, y)_{\mathcal{E}} = (X, Y)_{\mathbb{R}^n}$, где

    $x, y \in \mathcal{E}$ 

    $x \xrightarrow{e} X$

    $y \xrightarrow{e} Y$

    $e$ - ортонормированный базис.

2. Векторы ортогональны $\iff$ ортогональны их координатные столбцы в ортонормированном базисе.

<span class="stitle"> Доказательство </span>
1. $x = x_1e_1 + \ldots + x_ne_n$
    
    $y = y_1e_1 + \ldots + y_ne_n$
    
    $(x,y) = x_1y_1 + \ldots + x_ny_n = (X,Y)$, т.к. 
    $(e_i, e_j) = \begin{cases}
        0 & i \ne j \\
        1 & i = j
    \end{cases}$
    
2. Следует из первого пункта.

### Теорема. Процесс Ортогонализации Грама-Шмидта.
    
$\mathcal{E}; f=\{f_1, \ldots, f_k\}$ - ЛНЗ система векторов из $\mathcal{E}$. 
    
Можно построить ортонормированную систему векторов $e = \{e_1, \ldots, e_n\}$, каждый из которых $e_j \in \mathcal{L}(f_1, \ldots, f_k)$

<span class="stitle"> Доказательство: </span>

ММИ по количеству векторов.

1. $k = 1$: $f = \{f_1\}$; Пусть $e_1 = \frac{f_1}{|f_1|}$ получим $e = \{e_1\}$

2. Индукционный переход. Пусть справедливо для $m-1$, т.е. построили $\{e_1, \ldots, e_{m-1}\}
    \subset \mathcal{L}(f_1, \ldots, f_{m-1})$.



    Рассмотрим $\widetilde{f}_m = f_m - (c_1e_1 + \ldots + c_{m-1}e_{m-1})$. Этот вектор должен быть ортогонален всем предыдущим: $\forall j \in [1\ m-1    : (\widetilde{f}_m, e_j) = 0 \iff (f_m, e_j) = c_j \cdot |f_j|^2 = c_j$ (линейность по первому аргументу и факт ортогональности $e_j$ и $e{i \ne j}$    . 

    $\widetilde{f}_m \in \mathcal{L}(f_m, \underbrace{e_1, \ldots, e_{m-1}}_{\text{ЛК}}) \subset
    \mathcal{L}(f_1, \ldots, f_m)$

    $\widetilde{f}_m \ne \textbf{0}$, т.к. $\widetilde{f}_m$ представим в виде ЛК $f_1, \ldots, f_m$
    при чем коэффициент при $f_m$ не равен нулю (и система $\{f_1 \ldots f_m\}$ ЛНЗ).

    Пусть $e_m = \frac{\widetilde{f}_m}{|\widetilde{f}_m|} \in \mathcal{L}(f_1 \ldots f_m)$.
    $e = \{e_1 \ldots e_m\}$ - результат.