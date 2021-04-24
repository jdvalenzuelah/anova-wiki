---
title: "Anova 1 factor Completamenta Aleatorizado"
date: 2021-04-24T10:25:58-06:00
draft: false
---

# Modelo de Anova 1 factor Completamenta Aleatorizado

## Modelo

Cada observaciones del experimento se describen de con un modelo estadistico. 

$$
y_{ij} = \mu + \tau_i + e_{ijk} 
$$

#### Donde
- $y_{ij}$ = Es variable aleatoria que denoja ij-ésimas observación
- $\mu$ = Parametro que denota la media global
- $\tau_i$ = Efecto del i-ésimo tratamiento de y
- $\varepsilon_ij$ = Error aleatorio que se supone la normalidad, varianza constante e independencia.


# Plantamiento de Hipotesis
Se tienen 1 hipotesis en donde se plantean por medio de i-ésimas, y se toman la media global $\mu_i$ 

- $$H_o = \mu_i + \mu_i+1 ... \mu_n$$
- $$\text{Las medias no todas son iguales}$$

# Tabla de Anova

| Fuente u  origen de  la  variación | Suma de  Cuadrados ($SS$) | Grados  de  Libertad ($df$) | Media de  Cuadrados ($MS$) | F                    | F crítico                        | Valor P |
|------------------------------------|---------------------------|-----------------------------|----------------------------|----------------------|----------------------------------|---------|
| Tratamiento                                  | $SS_Tratamiento$                    | $g-1$                         | $MS_A=\frac{SS_Tratamient}{g-1}$    | $\frac{MS_Trata}{MS_e}$  | $F(\alpha, g-1, N-g)$        |         |
| Error                              | $SS_e=SS_{error}$         | $N-g$                   | $MS_e=\frac{SS_e}{(N-g)}$             |                      |                                  |         |
| Total                              | $SS_t=SS_{total}$         | $N-1$                       |                            |                      |                                  |         |

Se rechaza Ho cuando $F> F_critico$ o $Valor_p < \alpha$

# Calculo de Residuos
Residuo = $e_{ijk}$

$$e_{ijk}= dato \enspace observado - dato \enspace ajustado$$

# Gráficos de análisis de residuos

### Para verificar Normalidad:
- Histograma
- Grafico de probabilidad normal
- Resumen de Estadistica Descriptiva

### Para verificar varianza constante e independencia
- Residuo vs Niveles del Factor

# En ¿qué se diferencia este diseño de los otros?
Este modelo se diferencia en que solo se tiene un factor, por lo mismo dentro del analisis de residuo solo se hace una grafica de Residuo vs Tratamientos..

# Ejemplo
[Descargar](/anova-wiki/Ejemplo_2_k.xlsx)


