# stochastic-processes
\documentclass[12pt,a4paper,twoside]{article}

\usepackage[latin2]{inputenc}
\usepackage[spanish]{babel}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{graphicx}
\usepackage[left=4cm,right=2cm,top=2cm,bottom=2cm]{geometry}


\author{Kilian Huertas Cod: 624979 - Carlos Mora 625200}
\title{Taller Estocasticos}

\begin{document}

\maketitle 

Punto No. 1\\

a) Demuestre Experimentalmente la ley de los numeros grandes para un dado de 6 caras \\\\\ $\mu = E[X = ?]$\\

<br>$\blacksuqare$ Script Codigo realizado en C</br>

#include<winbgim.h>
#include<stdlib.h>
#include<iostream>
#include<fstream>
#include<cstdio>
#include<cstdlib>
#include<ctime>
#include <iomanip>
#include<conio.h>
using namespace std;

main(){
	setcolor(2);
	initwindow(1000,100);
	srand(time(NULL));
	float N[255];
	float Muestra[255];
	//float X[80];
	float Prom[255];
	float b,x,y;
	cout<<""<<"N"<<"\t"<<" Muestra"<<"  "<<"Promedio"<<"\t"<<endl;
	for (int i=1;i<=255;i++){
		N[i]=i;
		int Aleatorio = (rand()%6)+1;
		b=b+Aleatorio;
		for (int j=i;j<=255;j++){
			
			Muestra[j]=b;
			for (int k=i;k<255;k++){
				Prom[i]=(b/i);
				y=Prom[i];
			}
		}
		x=N[i];
		lineto(x*10,y*10);
		cout<<setw(1)<<N[i]<<"\t"<<"   "<<setw(1)<<Muestra[i]<<"\t"<<"   "<<setw(1)<<Prom[i]<<endl;
	}
	system("pause");
	closegraph();
	return 0;
}
</br>


(b) Cual es la diferencia entre la ley debil de los numeros grandes y la ley fuerte de los numeros grandes?

Las leyes de los numeros grandes describen el porqué de que el promedio de una muestra al azar de un evento cualquiera tenderá a estar muy cerca de la media  de los elementos del evento.
La ley debil debil de los numeros grandes denota que si la probabilidad de que ocurra un evento en una prueba única es p, y se hacen varias pruebas, independientemente la proporción mas probable de que ocurran los demas eventos en el número total de pruebas sera la misma probabilidad p; además, la varianza y el valor esperado poseen el mismo valor.
La ley  fuerte de los numeros grandes da a conocer la frecuencia relativa con que ocurre un evento en pruebas independientes y en las mismas condiciones converge a la probabilidad del evento observado con probabilidad 1, además el promedio de las variables aleatorias converge al valor esperado.

Punto No. 2

Demuestre que $E[X] $
$$ fx (x) = \frac{x^k-1 {e}^{-x/\Theta}} {\Theta \Gamma (k)} I (0,\infty) (x)$$


$ E [ x ] = (k)\Theta $


$ E [ x ]^2 = (k)\Theta^2 $


$ E [ x ] = \int\limits_ {-\infty}^\infty fx (x) = \int_0^\infty \mathrm{X} \frac{1}{\Theta \Gamma (k)} X^{(k-1)} {e}^{-x/\Theta} {\mathrm d x} = \frac{1}{\Theta^k \Gamma (k)}$


$\int_0^\infty \mathrm{X^k} {e}^{-x/\Theta}{\mathrm d x}$


$u= \frac{\mathrm x}{\mathrm \Theta}$


$x= u\Theta$


$ E [ x ] = \frac{1}{\Theta^k \Gamma (k)}\int_0^\infty \mathrm{u\Theta^k} {e}^u \Theta du \frac{\mathrm \Theta}{\mathrm \Gamma k} \int_0^\infty \mathrm{u^k} {e}^{-u} du = \frac{\Theta \Gamma (k+1)}{ \Gamma (k)} = {\Theta k}$


$ E [ x ]^2 = \int\limits_ {-\infty}^\infty {x^2 } f(x) dx = \int\limits_ {0}^\infty {x^2 } \frac{1}{\Theta^k \Gamma (k)} x^{k-1} {e}^{-k/\Theta} dx = \frac{1}{\Theta^k \Gamma (k)} \int\limits_ {0}^\infty x^{k+1} {e}^{-k/\Theta} dx$


$u= \frac{\mathrm x}{\mathrm \Theta}$

$x= u\Theta$


$dx= \Theta du$





Punto No. 3\\

a) Sea $X$ una variable aleatoria con funcion de densidad dada por:\\

$f[x]=\lbrace Ksin [\frac{1}{5} \pi X]$      Si $0\leqslant X \leqslant 5$\\

0		De otro modo\\

i) Determinar el valor de K.\\

$P(0\leqslant X \leqslant 5) = \displaystyle\int_a^b f(X)dx$\\

$\displaystyle\int_0^5 Ksin \frac {(\pi x)}{5} dx$\\

$k \displaystyle\int_0^5 sin \frac {(\pi x)}{5} dx$\\

$\frac {(5k)}{\pi} \displaystyle\int_0^5 u.du$\\

$- \frac {5k cos (\frac {(\pi x)}{5})}{\pi}$ remplazando en el rango de 0 to 5\\

$\frac {(10k)}{\pi}$\\

Igualamos a 1 la funcion\\

$\frac {(10k)}{\pi} = 1$\\

$k = \frac {(\pi)}{10}$\\

$k = 0.314$\\

ii) Varianza - Moda - Mediana - Media\\

Estado\\

$X = {0,1,2,3,4,5}$\\

$Moda = (\Phi)$ No existe\\

b) Sean dos dados corrientes simultaneamente. Sean X la variable aleatoria que denota la suma de los resultados obtenidos y B el evento definido por la suma de los resultados obtenidos que son divisibles por 3. Calcular $E=(X|B)$  

$X = $Sumas de los numeros obtenidos \\

$B = $Resultados Obtenidos divisibles por 3\\

$X(Sumas)---p(x)\\
2\longrightarrow\frac {1}{36}\\\\3\longrightarrow\frac {2}{36}\\\\4\longrightarrow\frac {3}{36}\\\\5\longrightarrow\frac {4}{36}\\\\6\longrightarrow\frac {5}{36}\\\\7\longrightarrow\frac {6}{36}\\\\8\longrightarrow\frac {5}{36}\\\\9\longrightarrow\frac {4}{36}\\\\10\longrightarrow\frac {3}{36}\\\\11\longrightarrow\frac {2}{36}\\\\12\longrightarrow\frac {1}{36}$\\

Posibles combinaciones\\

$B = [(2,1),(4,2),(2,4),(5,1),(1,5),(1,2)(6,3),(3,6),(3,3),(6,6),(5,4),(4,5)]$\\

$p(X|B) = \frac {(12)}{36}$\\

$E [X|B] = 3(\frac {2}{36})+6 (\frac {5}{36})+9(\frac {4}{36})+12(\frac {1}{36}) = \frac {7}{3} = 2.33$\\

\end{document}
