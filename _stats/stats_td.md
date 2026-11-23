<!-- source: td1_stats.md -->

# TD1 Stats

## Exercice 1

**Question A**

Car ces statistiques nécéssitent $n-1$ en tant que degrés de liberté.

**Question B**

Vers la vrai moyenne $\mu$ et écart-type $\sigma$

**Question C**

On peut le déterminer par $b = \frac{m}{s}$. Elle converge vers la vraie taille
d'effet $\beta$ de la population.

**Question D**

Vers 0.2 et pas en dessous, car l'erreur type représente l'écart entre
l'estimateur général d'erreur et la population vraie

**Question E**

La p-valeur diminue de plus en plus en fonction de l'augmentaiton de $n$, ce
qui veut dire que notre modèle réduit significativement l'erreur comparé à h0.
Elle s'écarte du seuil de significativité.

**Question F**

La population à une variance bien trop élevée, chaque échantillon donne donc des
estimations extrêment différentes et ne permettent pas d'agumenter la PRE. La
p-valeur ne diminue donc pas systématiquement et notre puissance statistique est
extrêmement faible.

**Question G**

Oui, le lien est inversé. Le $t$ de student correspond à la part d'erreur réduite
dans la taille d'effet observée.

**Question H**

On dirait que oui vu que c'est le même calcul

**Question I**

Il comprend pas systématiquement la vraie valeur

**Question J**

Car elle fluctue énormément

**Question K**

Non, proportionnellement à la baisse de la p-value

**Question L**

Car le carré moyen de l'erreur qui est utilisé pour le calculer est très haut je
crois ?

## Exercice 2

**Question A**

Vers une distribution normale

**Question B**

Normales dès une seule étude

**Question C**

Car toutes ces statistques sont des estimations issues d'une même population.
Chacune comporte une proportion d'erreur similaire autour d'une même moyenne
vraie, formant donc une normale.

**Question D**

L'erreur type est l'écart entre nos prédictions et les vraies valeurs,
comportant toujours donc uen proportion d'erreur et n'étant jamais 0. Il
faudrait connaître l'ensemble de la population sans erreur de mesure dans ce
cas.

**Question E**

Constant et principalement au-dessus de la valeur critique. $\mu = 0$ signifie
que la moyenne vraie de la population est de 0.

**Question F**

1

**Question G**

1, la différence est que les erreurs sont beaucoup plus grandes

**Question H**

5%, 5%, 0%, 0%

**Question I**

33%, 17%, 5%, 1%

**Question J**



---

- IA dans la recherche et les stats
- Conseils quarto et si ça va me faire des problèmes

---

<!-- source: td2_stats.md -->

# TD2 stats

## Question 1 ?

La régression n'a que des variables quantitatives.

Intercept est le point d'interception entre la droite et le point des ordonnées.
C'est surtout la VD moyenne prédite pour toute VI = 0. $b1$ est la pente du
modèle. C'est l'effet statistique brut. Ça représente de combien on gagne ou
perd sur la VD. Représente la force de l'association de la VD statistique entre
la VI et la VD. Effet satistique brut car il garde les unités des variables
d'origines. On différencie ceux-ci des effets dits standardisés. Le $d$ de cohen
représente différence standardisée entre des modalités de la VI.

Ici on va voir la corrélation de pearson, qui est standardisé car il n'a pas
l'unité de la VD/VI.

## Question 2

Résidues set ce qu'on calcule dans le numérateur du z-score. Pour les récolter

La somme du carré des résidus (H0) sera plus élevé que sous H1. Est-ce que la
PRE à un point est importante et pourquoi ?

## Question 4

On reperend les paramètres $b0$ et $b1$. La somme des résidus ne fait 0 qu'en
cas de droite moyenne. La somme des carrés des résidus est la plus élevé est h1
est plus faible systématiquement. On calcule la variance totale à partir de la
moyenne d'un jeu de donné. Les tests se demandent si l

Par définit la droite H1 minimise les erreurs commise et correpond au **BLUE** :
best linear unbiased estimator.

## Question 5

---

<!-- source: _td3_stats_fait_maison.md -->

# TD3 Stats

## Exercice 1 : Interprétation des résultats

Issu de la documentation `r` de `formula` :

> The models fitted by, e.g., the `lm` and `glm` functions are specified in a
> compact symbolic form. The `~` operator is basic in the formation of such
> models. An expression of the form `y ~ model` is interpreted as a
> specification that the response `y` is modelled by a **linear predictor**
> specified symbolically by `model`. Such a model consists of a series of terms
> separated by `+` operators. The terms themselves consist of variable and
> factor names separated by `:` operators. Such a term is interpreted as the
> interaction of all the variables and factors appearing in the term.

**$R^2$ = PRE = corrélation^2 !!!**

- A. child ~ 1 + parent **1**
- B.
  - a. **10**
  - b. 10
- C.
  - a. **11** donc n = 927
- D. 3
- E. 4
- F. 7
- G. 2
- H. 8
- I. 9
- J. 12
- K. lalal
- L. ll

## Exercice 2 : Indices, F de Fisher, hasard et inférence statistique

4. 5.32 et j'ai trouvé tout seul grâce à analyse de données je suis incroyable
5. Elle rétricit, car le F est basé sur le dénominateur 1-PRE/n-pa. Ici si n
   augmente, alors la part d'erreur réductible par paramètre aléatoire
   additionnel réduit, la valeur de PRE par paramètre du modèle est donc plus
   impressionnante. -> la je parle de valeur critique du F mais donc la
   distribution du F. En vérité **elle se tasse vers 0, moins de chance d'avoir
   de grandes valeurs** donc moins d'erreur de type 1, on peut donc rétrécir la
   valeur critique
6. L'inverse
7. Erreur car on aurait plus de -> **on ne peut même plus estimer les paramètres
   correctement. On parle de système non identifiable. Donc il faut des
   échantillons de grand taille pour des modèles complexes**

## Exercice 3

```{r}
#| label: test

lm()
```

---

<!-- source: td4_stats_fait_maison.md -->

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

