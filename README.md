# Software.

Encuentro  070422

dat <- read.csv("C:/Users/Lenovo/Downloads/PredictingToyotaPricesBlog-master/ToyotaCorolla.csv")
View(dat)

Primero se debe instalar el paquete "MVN" .
Este paquete es para ver si las variables son normales.

install.packages("MVN")
library(MVN)

Pedir los primeros cinco individuos 
dat[1:5,]
head(dat,n=5)

str(dat)

dat1<- dat[,c(1:3,5:10)]

Crear un gráfico de correlaciones

plot(dat1)


y <- dat[,c(1:3)]
y

Verficar normalidad a nivel multivariado 
y.nor<- mvn()

length(y$Price)


result <- mvn(data = y, mvnTest = "royston")
result$multivariateNormality
result$univariateNormality



g <- mvn(data = y, mvnTest = "royston", multivariateOutlierMethod = "quan")


w<- cor(y, method = "spearman")

Primero instalar el paquete "psych"
install.packages("psych")
library(psych)
library(ggplot2)
cor.plot(w, upper = FALSE, scale = F)

t<- as.numeric(w)




Debe de realizar un informe que contendrá la siguiente estructura
Este se debe de entregar el día jueves 21 a las 11: 50 pm
La cantidad de integrantes estará entre 3 hasta 4


Datos generales
I. Introducción
II. Desarrollo
III. Conclusiones
Bibliografía 


Para la tarea usted puede tomar elemetos de la siguiente publicación 

http://dataillumination.blogspot.com/2015/03/predictive-analytics-predicting-toyota.html

