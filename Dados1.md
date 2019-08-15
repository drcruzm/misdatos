---

## Definiciones Iniciales
```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = F)

install.packages("ggplot2")
install.packages("knitr")
library(knitr)    # Librerias a utilizar
library(ggplot2)  # library() # Librerias a utilizar
```

## Generando los Ensayos para la simulación Dado 1
```{r}
Ensayos <- 100
dado1 <- sample(x=1:6, size=Ensayos, replace=T, prob=NULL)
dado1
```

## Generando los Ensayos para la simulación Dado 2 
```{r}
dado2 <- sample(x=1:6, size=Ensayos, replace=T, prob=NULL)
dado2
```

## Suma de los Dados y Agrupando en Data Frame
```{r}
suma <- dado1 + dado2
suma
expdados <- data.frame(dado1,dado2,suma) #Haciendo el Data Frame
```

## Graficando los resultados de Experimento
```{r}
ggplot(expdados)+geom_bar(aes(dado1))
ggplot(expdados)+geom_bar(aes(dado2))
ggplot(expdados)+geom_bar(aes(suma))

```

## Calculo de valores estadísticos
```{r echo=FALSE}
st <- sd(suma) # Desviacion Estandar
st
xbar <- mean(suma) #Media muestra
xbar
```

## Histogramas
```{r echo=FALSE}
hist(suma, freq = F, col="gray")
grid(ny=20,col = 6)
x=expdados[,2]
mean(suma==7)
```

## Ajuste Normal
```{r echo=T}
hist(suma, freq = F)
curve(dnorm(x,xbar,st),col = 4,add = T)

```

## Simulación del Juego con ajuste Normal
```{r}
x.norm<-rnorm(n = 200,xbar,st)
hist(x.norm,main="Datos Simulados con Desv. Standar")
plot(density(x.norm),main="Densidad de Probabilidad Etimada")
plot(ecdf(x.norm),main="Funcion Empirica de distribucion acumulada")
```


