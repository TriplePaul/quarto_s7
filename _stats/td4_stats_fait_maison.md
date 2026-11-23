---
id: td4_stats_fait_maison
aliases:
  - td4_stats_fait_maison
tags: []
---

# td 4 stats fait maison

## Exercice 1

### A

Oui :

```r
#>       age        sexe       force
#>  Min.   :30.00   F:30   Min.   : 22.00
#>  1st Qu.:44.75   M:30   1st Qu.: 44.00
#>  Median :61.50          Median : 61.00
#>  Mean   :60.70          Mean   : 61.53
#>  3rd Qu.:74.50          3rd Qu.: 74.25
#>  Max.   :90.00          Max.   :110.00
```

### B

```r
#> Call:
#> lm(formula = force ~ 1 + age, data = donnees)
#>
#> Residuals:
#>     Min      1Q  Median      3Q     Max
#> -42.828 -17.348  -1.603  15.191  44.383
#>
#> Coefficients:
#>             Estimate Std. Error t value      Pr(>|t|)
#> (Intercept)  73.5072    10.6923   6.875 0.00000000476 ***
#> age          -0.1973     0.1694  -1.165         0.249
#> ---
#> Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
#>
#> Residual standard error: 22.74 on 58 degrees of freedom
#> Multiple R-squared:  0.02285,	Adjusted R-squared:  0.006003
#> F-statistic: 1.356 on 1 and 58 DF,  p-value: 0.2489
#>
```

L'âge à un effet très faible, de -0.2 environ. On ne peut pas rejeter h0 car la
valeur p est > à 0.05. $b_0$ est une mesure de la force moyenne (c'est le
paramètre qui réduit le plus la variance à partir de l'ensemble des données).

$b_0$ est la valeur de force pour âge = 0, ce qui n'a pas trop de sens dans
notre contexte car il porte sur une population qui es largement extrapolée.

### C

```r
#> 
#> Call:
#> lm(formula = force ~ 1 + sexe, data = donnees)
#> 
#> Residuals:
#>     Min      1Q  Median      3Q     Max 
#> -48.667 -11.467  -2.667  13.033  37.333 
#> 
#> Coefficients:
#>             Estimate Std. Error t value             Pr(>|t|)    
#> (Intercept)   61.533      2.585  23.807 < 0.0000000000000002 ***
#> sexe1         22.267      5.169   4.307            0.0000646 ***
#> ---
#> Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
#> 
#> Residual standard error: 20.02 on 58 degrees of freedom
#> Multiple R-squared:  0.2424,	Adjusted R-squared:  0.2293 
#> F-statistic: 18.55 on 1 and 58 DF,  p-value: 0.00006458
#> 
```

Sexe, en tant que facteurs, décrit un différence de 22.26 de force par niveau de
ce facteur. On peut rejeter H0.

### D

### E

### F
