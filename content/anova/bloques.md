---
title: "Bloques"
date: 2021-04-24T11:32:35-06:00
draft: false
---

# Modelo de anova

### Modelo:
$$
y_{ijk} = \mu + \tau_i + \beta_j + \epsilon_{ij}
\begin{cases}
    i = 1 ... a \\\\
    j = 1 ... b
\end{cases}
$$

#### Donde:
- $y_{ijk}$ denota la ijk-ésima observación
- $\mu$ es la media global
- $\tau_i$ es el efecto del tratamiento $i$
- $\beta_j$ es el efecto del block $j$
- $\epsilon_{ijk}$ es el componente de error aleatorio. Supone normalmente distribuido, con media cero, varianza constante e independientes.

# Planteamiento de hipótesis

$$
\text{Ho:}\enspace\mu_1 = \mu_2 = ...\mu_a\\\\
\text{Ha:}\enspace No \enspace todas \enspace las \enspace medias \enspace son \enspace iguales
$$

# Tabla Anova

| Fuente u  origen de  la  variación | Suma de  Cuadrados ($SS$)           | Grados  de  Libertad ($df$) | Media de  Cuadrados ($MS$) | F                |
|------------------------------------|-------------------------------------|-----------------------------|----------------------------|------------------|
| Tratamientos                       | $SS_{trat}$                         | $a-1$                       | $MS_{Trat}$                | $MS_{trat}/MS_e$ |
| Bloques                            | $SS_{block}$                        | $b-1$                       | $MS_{block}$               |                  |
| Error                              | $SS_e=SS_{error}$                   | $(a-1)((b-1)$               | $MS_e$                     |                  |
| Total                              | $SS_t=S_{trat} + SS_{Block} + SS_e$ | $N-1$                       |                            |                  |

# Cálculo de residuos

$$e_{ij}=y_{ij}-(\bar{y}_{i*} + \bar{y}_{j*} - \bar{y}_{**}) \\\\ 
donde \enspace (\bar{y}_{i*} + \bar{y}_{j*} - \bar{y}_{**}) = \text{valor ajustado}
$$

# Gráficos de análisis de residuos

### Para verificar Normalidad:
- Histograma
- Grafico de probabilidad normals

### Para verificar varianza constante e independencia
- Residuo vs Valor ajustado
- Residuos vs Factor A

# En ¿qué se diferencia este diseño de los otros?

Este modelo se diferencia en que solo se esta evaluando 1 factor, pero que puede ser afectado por otro factor. Para esto se "bloquea" el factor indeseado para determinar el efecto del factor que se quiere evaluar, sin que el factor indeseado pueda afectar nuestras conclusiones.

# Ejemplo
[Descargar](/anova-wiki/Ejemplo_2_k.xlsx)