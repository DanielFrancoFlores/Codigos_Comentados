# Documentancion de codigo

#### Daniel Rigoberto Franco Flores 

Los datos de la Secretaría de Economía, relacionado a la producción de las N fábricas en cada uno de los meses del año anterior, en este problema nos plantean diferentes resoluciones o problemas a resolver que veremos a continuación:

Para comenzar con el codigo, incluiremos las siguientes librerias y declaraciones en c++:
```cpp
#include <iostream>
using namespace std;
```
En esta seccion, dentro del main, declaramos las siguientes variables:
```cpp
int main() { 
const int meses = 12;  
int N; 
```
En esta etapa del codigo estaremos leyendo el numero de fabricas a analizar
```cpp
cout << "¿Cuántas fábricas tendrá el arreglo?: "; 
cin >> N; 
```
En esta seccion del codigo declaramos las siguientes matrices:
```cpp
int FABRICAS[N]; 
float VentasMes[N][meses];
 ```
 
 A continuacion, en la siguiente parte del codigo, se hace una lectura de datos, tanto para las claves de las fabricas como para las ventas por mes de cada fabrica, el cual para leer matrices o vectores bidimensionales se usan ciclos for
```cpp
// Lectura de las claves de las fábricas 
cout << "Introduzca las claves de las fábricas:" << endl; 
for (int i = 0; i < N; i++) { 
cout << "[" << i << "]: "; 
cin >> FABRICAS[i]; 
}
// Lectura de las ventas por mes de cada fábrica
cout << "Introduzca las ventas de las fábricas por mes:" << endl; 
for (int i = 0; i < N; i++) { 
cout << "Fábrica " << FABRICAS[i] << ":" << endl; 
	for (int j = 0; j < meses; j++) { 
		cout << "Mes " << (j + 1) << ": "; 
		cin >> VentasMes[i][j]; 
	} 
}
 ```
 
 Para el primer problema que se nos presenta nos indican **encontar la fabrica que mas produjo.**
 Para iniciar, creamos nuvas variables y las inicializamos para este problema, donde uno indicara el indice y el otro se tomara como un mayor
 ```cpp
int indiceFabricaMayor = 0;
float mayorProduccion = VentasMes[0][0];
 ```
 
Este seria el calculo para llegar a encontrar la fabrica que mas produjo en el año, podemos observar que se usa un ciclo for para iterar en la matriz y un if para poder hacer comparaciones y llegar a la fabrica que mas produjo en el año
 ```cpp
 for (int i = 0; i < N; i++) {
		 for (int j = 0; j < meses; j++) {
			 if (VentasMes[i][j] > mayorProduccion) {
				 mayorProduccion = VentasMes[i][j];
				 indiceFabricaMayor = i;
			 }
		}
}
```

Esta vendria siendo la impresion en pantalla donde muestra la clave de la fabrica que mas produjo en el año pasado y cuanto fue lo que produjo
 ```cpp
 cout << "La fábrica que más produjo fue la clave " << FABRICAS[indiceFabricaMayor]
		 << " con una producción de " << mayorProduccion << endl;
 ```

Para el segundo problema que se nos plantea **encontra las fabricas que superaron cierta produccion en un mes** que este caso es de **150000**
 ```cpp
 const float ProduccionSuperior = 150000;
 int mesInteres;
 ```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MjY4MTU5MTUsLTE5NTExMjM4MjYsLT
k1ODM3MzkwLC0xMDY4OTQyODAsLTE3NDYwMjkyNiwtMjA4ODc0
NjYxMiwyNjM4MzY5MDksNDcwODI1MDczLC0zMzI0NTUzNjNdfQ
==
-->