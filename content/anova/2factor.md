---
title: "Anova 2 factores"
date: 2021-04-21T16:29:25-06:00
draft: false
---

# Modelo de anova

Suponiendo que tenemos:
- Factor A con a niveles
- Factor B con b niveles
- n replicas

### Modelo:
$$
y_{ijk} = \mu + \alpha_i + \beta_j + (\alpha \beta)_{ij} + e_{ijk} \enspace
\begin{cases}
    i = 1 ... a \\\\
    j = 1 ... b \\\\
    k = 1 ... n
\end{cases}
$$

#### Donde:
- $y_{ijk}$ denota la ijk-ésima observación
- $\mu$ es la media global
- $\alpha_i$ es un parámetro asociado al i-ésimo nivel del factor A
- $\beta_j$ es un parámetro asociado al j-ésimo nivel del factor B
- $(\alpha \beta)_{ij}$  s un parámetro asociado al ij-ésimo tratamiento del nivel i de A con el nivel j de B
- $e_{ijk}$ es el componente de error aleatorio. Supone normalmente distribuido, con media cero, varianza constante e independientes.

# Planteamiento de hipótesis

Se tendran 3 juegos de hipotesis, para el factor A, B y el factor de interaccion AB.

#### Para el factor A:
$$
\text{Ho:}\enspace\sum_{i = 1}^{a} \alpha_i = 0 \\\\
\text{Ha:}\enspace\alpha_i \neq 0 \enspace\text{para algún}\enspace i
$$

#### Para el factor B:
$$
\text{Ho:}\enspace\sum_{j = 1}^{b} \beta_j = 0 \\\\
\text{Ha:}\enspace\beta_j \neq 0 \enspace\text{para algún}\enspace j
$$

#### Para el factor de intereaccion AB:
$$
\text{Ho:}\enspace\sum_{i = 1}^{a}\sum_{j = 1}^{b} (\alpha\beta)_{ij} = 0 \\\\
\text{Ha:}\enspace(\alpha\beta)_{ij} \neq 0 \enspace\text{para algún}\enspace ij
$$

# Tabla Anova

| Fuente u  origen de  la  variación | Suma de  Cuadrados ($SS$) | Grados  de  Libertad ($df$) | Media de  Cuadrados ($MS$) | F                    | F crítico                        | Valor P |
|------------------------------------|---------------------------|-----------------------------|----------------------------|----------------------|----------------------------------|---------|
| A                                  | $SS_A$                    | $a$                         | $MS_A=\frac{SS_A}{a-1}$    | $\frac{MS_A}{MS_e}$  | $F(\alpha, a-1, ab(n-1))$        |         |
| B                                  | $SS_B$                    | $b$                         | $MS_B=\frac{SS_B}{b-1}$    | $\frac{MS_B}{MS_e}$  | $F(\alpha, b-1, ab(n-1))$        |         |
| AB                                 | $SS_{AB}$                 | $(a-1)(b-1)$                | $MS_{AB}=(a-1)(b-1)$       | $\frac{MS_AB}{MS_e}$ | $F(\alpha, (a-1)(b-1), ab(n-1))$ |         |
| Error                              | $SS_e=SS_{error}$         | $ab(n-1)$                   | $MS_e=ab(n-1)$             |                      |                                  |         |
| Total                              | $SS_t=SS_{total}$         | $N-1$                       |                            |                      |                                  |         |

# Cálculo de residuos

Residuo = $e_{ijk}$

$$e_{ijk}= dato \enspace observado - dato \enspace ajustado$$

$$e_{ijk}= y_{ijk} - promedio \enspace de \enspace la \enspace combinación \enspace de \enspace tratamiento$$

# Gráficos de análisis de residuos

### Para verificar Normalidad:
- Histograma
- Grafico de probabilidad normal

### Para verificar varianza constante e independencia
- Residuo vs Valor ajustado
- Residuos vs Factor A
- Residuos vs Factor B
- Residuos vs Factor de interaccion AB

### Para verificar independencia
- Residuos vs Orden de corrida

# En ¿qué se diferencia este diseño de los otros?

Este modelo se diferencia en que solo se puede trabjar cuando se tienen 2 factores, pero cualquier numero de niveles para cualquiera de los 2 factores, con este analisis podemos obtener 


# Ejemplo
[Descargar](/anova-wiki/Ejemplo_2_k.xlsx)