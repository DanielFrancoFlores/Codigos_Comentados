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

Para el segundo problema que se nos plantea **encontra las fabricas que superaron cierta produccion en un mes** que este caso es de **150000** y el mes que nos interesara saber o investigar
 ```cpp
 const float ProduccionSuperior = 150000;
 int mesInteres;
 ```
 
Aqui leemos al mes que queremos hacer referencia
 ```cpp
cout << "¿En qué mes desea saber la producción de las fábricas?: ";
cin >> mesInteres; // Se lee el mes de interés
 ```

Esta parte del codigo, muestra los calculos y muestra el codigo de las fabricas que superaron la canttidad de produccion al mes, esto se logra con un ciclo for para las claves de las empresas y con una comparacion hecha por un if de si la produccion hecha en ese mes es superior a 150000
```cpp
cout << "Las fábricas que superaron una producción de " << ProduccionSuperior
		<< " en el mes " << mesInteres << " son:" << endl;
for (int i = 0; i < N; i++) {
	if (VentasMes[i][mesInteres - 1] > ProduccionSuperior) {
			cout << "Clave de fábrica: " << FABRICAS[i] << endl;
	}
}
```

Para el t problema se nos plantea lo siguiente **
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NjUxNjcxNCwtNjc5MTg5MTIyLC0yOD
AwNjc0NzUsLTE2Mjg5MTkzODcsLTcyMzI5ODc1MiwtMTQyNjgx
NTkxNSwtMTk1MTEyMzgyNiwtOTU4MzczOTAsLTEwNjg5NDI4MC
wtMTc0NjAyOTI2LC0yMDg4NzQ2NjEyLDI2MzgzNjkwOSw0NzA4
MjUwNzMsLTMzMjQ1NTM2M119
-->