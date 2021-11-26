Tarea 2
================
Xilene Cocha Morales
25/11/2021

# **Ejercicios**

1.  ¿Qué cantidad de dinero sobra al repartir 10000$ entre 3 personas?

``` r
10000 %% 3
```

    ## [1] 1

2.  ¿Es el núumero 4560 divisible por 3?

``` r
x <- 4560
function(x) x[x %% 3 == 0]
```

    ## function(x) x[x %% 3 == 0]

``` r
div_3 <- function(x) x[x %% 3 == 0]
div_3(x)
```

    ## [1] 4560

3.  Construya un vector con los núumeros enteros del 2 al 87. ¿Cuáles de
    esos números son divisibles por 7?

``` r
2:87
```

    ##  [1]  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26
    ## [26] 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51
    ## [51] 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76
    ## [76] 77 78 79 80 81 82 83 84 85 86 87

``` r
   x <- (2:87)
   for (x in 2:87){
     if (x%%7 == 0){
       print(x)
       
     }
   }
```

    ## [1] 7
    ## [1] 14
    ## [1] 21
    ## [1] 28
    ## [1] 35
    ## [1] 42
    ## [1] 49
    ## [1] 56
    ## [1] 63
    ## [1] 70
    ## [1] 77
    ## [1] 84

4.  Construya dos vectores, el primero con los números enteros desde 7
    hasta 3, el segundo vector con los primeros cinco números positivos
    divisibles por 5.

-   Sea A la condición de ser par en el primer vector.

``` r
c(7:3)
```

    ## [1] 7 6 5 4 3

``` r
l = (7:3)
for (x in 7:3) {
  if (x%%2 == 0) {
    print(x)
  }
}
```

    ## [1] 6
    ## [1] 4

``` r
l%%2 == 0
```

    ## [1] FALSE  TRUE FALSE  TRUE FALSE

-   Sea B la condición de ser mayor que 10 en el segundo vector.

``` r
m= c(5, 10, 15, 20, 25)
m > 10
```

    ## [1] FALSE FALSE  TRUE  TRUE  TRUE

-   ¿En cuál de las 5 posiciones se cumple A y B simultáneamente?

``` r
which(m > 10 & l%%2 == 0)
```

    ## [1] 4

5.  Consulte este
    [Link](https://github.com/fhernanb/Manual-de-R/blob/master/images/anecdota_gauss.PNG)
    en el cual hay una anéctoda de Gauss niño. Use R para obtener el
    resultado de la suma solicitada por el profesor del niño Gauss.

``` r
g <- 1:100
sum(g)
```

    ## [1] 5050

6.  Construya un vector con los siguientes elementos: 1, -4, 5, 9, -4.
    Escriba un procedimiento para extraer las posiciones donde está el
    valor mínimo en el vector.

``` r
#procedimiento
# a) Crear un vector con los números que brindan de dato.
c(1, -4, 5, 9, -4)
```

    ## [1]  1 -4  5  9 -4

``` r
# b) Asignar una variable al vector
vect <- c(1, -4, 5, 9, -4)
# c) Hallar cuál es el valor mínimo del vector, con la función min()
min(vect)
```

    ## [1] -4

``` r
# d) Una vez conocido el valor mínino del vector. Hallar las posiciones donde se encuentra este número en el vector, para ello usar la función which()
which(vect == -4)
```

    ## [1] 2 5

7.  Calcular 8!

``` r
factorial(8)
```

    ## [1] 40320

8.  Evaluar la siguiente sumatoria

``` r
a <- c(3,4,5,6,7)
sum(exp(a))
```

    ## [1] 1723.159

9.Evaluar la siguiente productoria

``` r
 prod(1:10)
```

    ## [1] 3628800

``` r
 sqrt(1:10)
```

    ##  [1] 1.000000 1.414214 1.732051 2.000000 2.236068 2.449490 2.645751 2.828427
    ##  [9] 3.000000 3.162278

``` r
 log(sqrt(1:10))
```

    ##  [1] 0.0000000 0.3465736 0.5493061 0.6931472 0.8047190 0.8958797 0.9729551
    ##  [8] 1.0397208 1.0986123 1.1512925

10. Realizar una función que permita calcular el área de una corona
    circular.

11. Construya un vector cualquiera e inviertalo, es decir, que el primer
    elemento quede de ́ultimo, el segundo de penúltimo y así
    sucesivamente. Compare su resultado con el de la función rev()

``` r
e <- c(23,22,21,19,12)
sort(e)
```

    ## [1] 12 19 21 22 23

``` r
rev(e)
```

    ## [1] 12 19 21 22 23

12. Calcular lo siguiente

``` r
b <- 10:100
c <- (b^3)
d <- (4*b^2)
sum(c + d)
```

    ## [1] 26852735

13. Calcular lo siguiente

``` r
a <- 1:25
((2^a)/a)+((3^a)/a^2)
```

    ##  [1] 5.000000e+00 4.250000e+00 5.666667e+00 9.062500e+00 1.612000e+01
    ##  [6] 3.091667e+01 6.291837e+01 1.345156e+02 2.998889e+02 6.928900e+02
    ## [11] 1.650207e+03 4.031896e+03 1.006402e+04 2.557319e+04 6.595745e+04
    ## [16] 1.722473e+05 4.545619e+05 1.210306e+06 3.247155e+06 8.769390e+06
    ## [21] 2.381949e+07 6.502755e+07 1.783291e+08 4.910281e+08 1.357004e+09

``` r
jd <- ((2^a)/a)+((3^a)/a^2)
sum(jd)
```

    ## [1] 2129170437

14. Lea el siguiente
    [Archivo](https://raw.githubusercontent.com/fhernanb/datos/master/Paises.txt)

``` r
read.delim("https://raw.githubusercontent.com/fhernanb/datos/master/Paises.txt")
```

    ##                 Pais poblacion alfabetizacion tasamortinf   PIB
    ## 1         Acerbaján_      7400             98        35.0  3000
    ## 2         Afganistán     20500             29       168.0   205
    ## 3           Alemania     81200             99         6.5 17539
    ## 4       Arabia_Saudí     18000             62        52.0  6651
    ## 5         Argentina_     33900             95        25.6  3408
    ## 6           Armenia_      3700             98        27.0  5000
    ## 7         Australia_     17800            100         7.3 16848
    ## 8           Austria_      8000             99         6.7 18396
    ## 9           Bahrein_       600             77        25.0  7875
    ## 10        Bangladesh    125000             35       106.0   202
    ## 11          Barbados       256             99        20.3  6950
    ## 12          Bélgica_     10100             99         7.2 17912
    ## 13        Bielorusia     10300             99        19.0  6500
    ## 14          Bolivia_      7900             78        75.0   730
    ## 15            Bosnia      4600             86        12.7  3098
    ## 16          Botswana      1359             72        39.3  2677
    ## 17            Brasil    156600             81        66.0  2354
    ## 18          Bulgaria      8900             93        12.0  3831
    ## 19      Burkina_Faso     10000             18       118.0   357
    ## 20          Burundi_      6000             50       105.0   208
    ## 21          Camboya_     10000             35       112.0   260
    ## 22          Camerún_     13100             54        77.0   993
    ## 23            Canadá     29100             97         6.8 19904
    ## 24            Chile_     14000             93        14.6  2591
    ## 25            China_   1205200             78        52.0   377
    ## 26          Colombia     35600             87        28.0  1538
    ## 27  Corea_del_Norte_     23100             99        27.7  1000
    ## 28    Corea_del_Sur_     45000             96        21.7  6627
    ## 29        Costa_Rica      3300             93        11.0  2031
    ## 30          Croacia_      4900             97         8.7  5487
    ## 31              Cuba     11100             94        10.2  1382
    ## 32        Dinamarca_      5200             99         6.6 18277
    ## 33          Ecuador_     10700             88        39.0  1085
    ## 34            Egipto     60000             48        76.4   748
    ## 35      El_Salvador_      5800             73        41.0  1078
    ## 36  Emiratos_Árabes_      2800             68        22.0 14193
    ## 37            España     39200             95         6.9 13047
    ## 38    Estados_Unidos    260800             97         8.1 23474
    ## 39          Estonia_      1600             99        19.0  6000
    ## 40          Etiopía_     55200             24       110.0   122
    ## 41        Filipinas_     69800             90        51.0   867
    ## 42        Finlandia_      5100            100         5.3 15877
    ## 43          Francia_     58000             99         6.7 18944
    ## 44            Gabón_      1300             61        94.0  4283
    ## 45            Gambia       959             27       124.0   351
    ## 46          Georgia_      5500             99        23.0  4500
    ## 47      Gran_Bretaña     58400             99         7.2 15974
    ## 48            Grecia     10400             93         8.2  8060
    ## 49        Guatemala_     10300             55        57.0  1342
    ## 50            Haití_      6500             53       109.0   383
    ## 51          Honduras      5600             73        45.0  1030
    ## 52        Hong_Kong_      5800             77         5.8 14641
    ## 53            Hungía     10500             99        12.5  5249
    ## 54            India_    911600             52        79.0   275
    ## 55        Indonesia_    199700             77        68.0   681
    ## 56              Irán     65600             54        60.0  1500
    ## 57              Iraq     19900             60        67.0  1955
    ## 58          Irlanda_      3600             98         7.4 12170
    ## 59          Islandia       263            100         4.0 17241
    ## 60            Israel      5400             92         8.6 13066
    ## 61            Italia     58100             97         7.6 17500
    ## 62            Japón_    125500             99         4.4 19860
    ## 63          Jordania      3961             80        34.0  1157
    ## 64            Kenia_     28200             69        74.0   323
    ## 65            Kuwait      1800             73        12.5  6818
    ## 66          Letonia_      2700             99        21.5  7400
    ## 67            Líbano      3620             80        39.5  1429
    ## 68          Liberia_      2900             40       113.0   409
    ## 69            Libia_      5500             64        63.0  5910
    ## 70          Lituania      3800             99        17.0  6710
    ## 71          Malasia_     19500             78        25.6  2995
    ## 72        Marruecos_     28600             50        50.0  1062
    ## 73            México     91800             87        35.0  3604
    ## 74        Nicaragua_      4100             57        52.5   447
    ## 75          Nigeria_     98100             51        75.0   282
    ## 76          Noruega_      4300             99         6.3 17755
    ## 77    Nueva_Zelanda_      3524             99         8.9 14381
    ## 78      Países_Bajos     15400             99         6.3 17245
    ## 79          Pakistán    128100             35       101.0   406
    ## 80            Panamá      2600             88        16.5  2397
    ## 81          Paraguay      5200             90        25.2  1500
    ## 82              Perú     23650             85        54.0  1107
    ## 83          Polonia_     38600             99        13.8  4429
    ## 84          Portugal     10500             85         9.2  9000
    ## 85  Rep._C._Africana      3300             27       137.0   457
    ## 86  Rep._Dominicana_      7800             83        51.5  1034
    ## 87            Ruanda      8400             50       117.0   292
    ## 88          Rumanía_     23400             96        20.3  2702
    ## 89            Rusia_    149200             99        27.0  6680
    ## 90          Senegal_      8700             38        76.0   744
    ## 91          Singapur      2900             88         5.7 14990
    ## 92            Siria_     14900             64        43.0  2436
    ## 93          Somalia_      6667             24       126.0  2126
    ## 94        Sudáfrica_     43900             76        47.1  3128
    ## 95            Suecia      8800             99         5.7 16900
    ## 96            Suiza_      7000             99         6.2 22384
    ## 97        Tailandia_     59400             93        37.0  1800
    ## 98            Taiwan     20944             91         5.1  7055
    ## 99          Tanzania     29800             46       110.0   263
    ## 100         Turquía_     62200             81        49.0  3721
    ## 101         Ucrania_     51800             97        20.7  2340
    ## 102           Uganda     19800             48       112.0   325
    ## 103         Uruguay_      3200             96        17.0  3131
    ## 104       Uzbekistán     22600             97        53.0  1350
    ## 105       Venezuela_     20600             88        28.0  2829
    ## 106         Vietnam_     73100             88        46.0   230
    ## 107           Zambia      9100             73        85.0   573

``` r
df <- read.delim("https://raw.githubusercontent.com/fhernanb/datos/master/Paises.txt")
class(df)
```

    ## [1] "data.frame"

-   Calcular el número de variables del dataset

``` r
length(df)
```

    ## [1] 5

-   ¿Cuántos países hay en el dataset?

``` r
df$Pais
```

    ##   [1] "Acerbaján_"       "Afganistán"       "Alemania"        
    ##   [4] "Arabia_Saudí"     "Argentina_"       "Armenia_"        
    ##   [7] "Australia_"       "Austria_"         "Bahrein_"        
    ##  [10] "Bangladesh"       "Barbados"         "Bélgica_"        
    ##  [13] "Bielorusia"       "Bolivia_"         "Bosnia"          
    ##  [16] "Botswana"         "Brasil"           "Bulgaria"        
    ##  [19] "Burkina_Faso"     "Burundi_"         "Camboya_"        
    ##  [22] "Camerún_"         "Canadá"           "Chile_"          
    ##  [25] "China_"           "Colombia"         "Corea_del_Norte_"
    ##  [28] "Corea_del_Sur_"   "Costa_Rica"       "Croacia_"        
    ##  [31] "Cuba"             "Dinamarca_"       "Ecuador_"        
    ##  [34] "Egipto"           "El_Salvador_"     "Emiratos_Árabes_"
    ##  [37] "España"           "Estados_Unidos"   "Estonia_"        
    ##  [40] "Etiopía_"         "Filipinas_"       "Finlandia_"      
    ##  [43] "Francia_"         "Gabón_"           "Gambia"          
    ##  [46] "Georgia_"         "Gran_Bretaña"     "Grecia"          
    ##  [49] "Guatemala_"       "Haití_"           "Honduras"        
    ##  [52] "Hong_Kong_"       "Hungía"           "India_"          
    ##  [55] "Indonesia_"       "Irán"             "Iraq"            
    ##  [58] "Irlanda_"         "Islandia"         "Israel"          
    ##  [61] "Italia"           "Japón_"           "Jordania"        
    ##  [64] "Kenia_"           "Kuwait"           "Letonia_"        
    ##  [67] "Líbano"           "Liberia_"         "Libia_"          
    ##  [70] "Lituania"         "Malasia_"         "Marruecos_"      
    ##  [73] "México"           "Nicaragua_"       "Nigeria_"        
    ##  [76] "Noruega_"         "Nueva_Zelanda_"   "Países_Bajos"    
    ##  [79] "Pakistán"         "Panamá"           "Paraguay"        
    ##  [82] "Perú"             "Polonia_"         "Portugal"        
    ##  [85] "Rep._C._Africana" "Rep._Dominicana_" "Ruanda"          
    ##  [88] "Rumanía_"         "Rusia_"           "Senegal_"        
    ##  [91] "Singapur"         "Siria_"           "Somalia_"        
    ##  [94] "Sudáfrica_"       "Suecia"           "Suiza_"          
    ##  [97] "Tailandia_"       "Taiwan"           "Tanzania"        
    ## [100] "Turquía_"         "Ucrania_"         "Uganda"          
    ## [103] "Uruguay_"         "Uzbekistán"       "Venezuela_"      
    ## [106] "Vietnam_"         "Zambia"

``` r
length(df$Pais)
```

    ## [1] 107

-   ¿Cuál es el país con mayor población?

``` r
max(df$poblacion)
```

    ## [1] 1205200

``` r
which(df$poblacion == 1205200)
```

    ## [1] 25

``` r
df$Pais
```

    ##   [1] "Acerbaján_"       "Afganistán"       "Alemania"        
    ##   [4] "Arabia_Saudí"     "Argentina_"       "Armenia_"        
    ##   [7] "Australia_"       "Austria_"         "Bahrein_"        
    ##  [10] "Bangladesh"       "Barbados"         "Bélgica_"        
    ##  [13] "Bielorusia"       "Bolivia_"         "Bosnia"          
    ##  [16] "Botswana"         "Brasil"           "Bulgaria"        
    ##  [19] "Burkina_Faso"     "Burundi_"         "Camboya_"        
    ##  [22] "Camerún_"         "Canadá"           "Chile_"          
    ##  [25] "China_"           "Colombia"         "Corea_del_Norte_"
    ##  [28] "Corea_del_Sur_"   "Costa_Rica"       "Croacia_"        
    ##  [31] "Cuba"             "Dinamarca_"       "Ecuador_"        
    ##  [34] "Egipto"           "El_Salvador_"     "Emiratos_Árabes_"
    ##  [37] "España"           "Estados_Unidos"   "Estonia_"        
    ##  [40] "Etiopía_"         "Filipinas_"       "Finlandia_"      
    ##  [43] "Francia_"         "Gabón_"           "Gambia"          
    ##  [46] "Georgia_"         "Gran_Bretaña"     "Grecia"          
    ##  [49] "Guatemala_"       "Haití_"           "Honduras"        
    ##  [52] "Hong_Kong_"       "Hungía"           "India_"          
    ##  [55] "Indonesia_"       "Irán"             "Iraq"            
    ##  [58] "Irlanda_"         "Islandia"         "Israel"          
    ##  [61] "Italia"           "Japón_"           "Jordania"        
    ##  [64] "Kenia_"           "Kuwait"           "Letonia_"        
    ##  [67] "Líbano"           "Liberia_"         "Libia_"          
    ##  [70] "Lituania"         "Malasia_"         "Marruecos_"      
    ##  [73] "México"           "Nicaragua_"       "Nigeria_"        
    ##  [76] "Noruega_"         "Nueva_Zelanda_"   "Países_Bajos"    
    ##  [79] "Pakistán"         "Panamá"           "Paraguay"        
    ##  [82] "Perú"             "Polonia_"         "Portugal"        
    ##  [85] "Rep._C._Africana" "Rep._Dominicana_" "Ruanda"          
    ##  [88] "Rumanía_"         "Rusia_"           "Senegal_"        
    ##  [91] "Singapur"         "Siria_"           "Somalia_"        
    ##  [94] "Sudáfrica_"       "Suecia"           "Suiza_"          
    ##  [97] "Tailandia_"       "Taiwan"           "Tanzania"        
    ## [100] "Turquía_"         "Ucrania_"         "Uganda"          
    ## [103] "Uruguay_"         "Uzbekistán"       "Venezuela_"      
    ## [106] "Vietnam_"         "Zambia"

``` r
df$Pais[25]
```

    ## [1] "China_"

-   ¿Cuál es el país con alfabetización más baja?

``` r
min(df$alfabetizacion)
```

    ## [1] 18

``` r
which(df$alfabetizacion == 18)
```

    ## [1] 19

``` r
df$Pais[19] 
```

    ## [1] "Burkina_Faso"

15. En R hay unas bases de datos incluídas, una de ellas es la base de
    datos llamada mtcars. Para conocer las variables que están en mtcars
    usted puede escribir en la consola ?mtcars o también help(mtcars).
    De la base mtcars obtenga bases de datos que cumplan las siguientes
    condiciones.

``` r
df_mtcars <- mtcars
```

-   Autos que tengan un rendimiento menor a 18 millas por galón de
    combustible.

``` r
df_mtcars$mpg
```

    ##  [1] 21.0 21.0 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 17.8 16.4 17.3 15.2 10.4
    ## [16] 10.4 14.7 32.4 30.4 33.9 21.5 15.5 15.2 13.3 19.2 27.3 26.0 30.4 15.8 19.7
    ## [31] 15.0 21.4

``` r
df_mtcars[(df_mtcars$mpg < 18),]
```

    ##                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    ## Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
    ## Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
    ## Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
    ## Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
    ## Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
    ## Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
    ## Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
    ## Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
    ## Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
    ## AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
    ## Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
    ## Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
    ## Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8

-   Autos que tengan 4 cilíndros

``` r
df_mtcars$cyl
```

    ##  [1] 6 6 4 6 8 6 8 4 4 6 6 8 8 8 8 8 8 4 4 4 4 8 8 8 8 4 4 4 8 6 8 4

``` r
df_mtcars[(df_mtcars$cyl==4),]
```

    ##                 mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    ## Datsun 710     22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
    ## Merc 240D      24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
    ## Merc 230       22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
    ## Fiat 128       32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
    ## Honda Civic    30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
    ## Toyota Corolla 33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
    ## Toyota Corona  21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
    ## Fiat X1-9      27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
    ## Porsche 914-2  26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
    ## Lotus Europa   30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
    ## Volvo 142E     21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2

-   Autos que pesen más de 2500 libras y tengan transmisión manual.

``` r
df_mtcars$wt
```

    ##  [1] 2.620 2.875 2.320 3.215 3.440 3.460 3.570 3.190 3.150 3.440 3.440 4.070
    ## [13] 3.730 3.780 5.250 5.424 5.345 2.200 1.615 1.835 2.465 3.520 3.435 3.840
    ## [25] 3.845 1.935 2.140 1.513 3.170 2.770 3.570 2.780

``` r
df_mtcars[(df_mtcars$wt > 2.500) & (df_mtcars$am==1),]
```

    ##                 mpg cyl disp  hp drat    wt  qsec vs am gear carb
    ## Mazda RX4      21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
    ## Mazda RX4 Wag  21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
    ## Ford Pantera L 15.8   8  351 264 4.22 3.170 14.50  0  1    5    4
    ## Ferrari Dino   19.7   6  145 175 3.62 2.770 15.50  0  1    5    6
    ## Maserati Bora  15.0   8  301 335 3.54 3.570 14.60  0  1    5    8
    ## Volvo 142E     21.4   4  121 109 4.11 2.780 18.60  1  1    4    2

16. La ecuación de tiempo es la diferencia entre el tiempo solar medio y
    el tiempo solar aparente
    [Referencia](http://pbarbier.com/eqtime/eqtime.html).Si bien esta
    varía, la forma analítica de esta ecuación se muestra a continuación
    (Usar x como un rango de 0 a 365). Replicar el gráfico: *y = 2π · (x
    − 81)/365* *f(y) = 9.87 · sin(2y) − 7.53 · cos(y) − 1.5 · sin(y)*
