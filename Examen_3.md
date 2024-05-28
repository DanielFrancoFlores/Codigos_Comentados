# Documentación de código

  #### Daniel Rigoberto Franco Flores
Los datos de la Secretaría de Economía, relacionado a la producción de las N fábricas en cada uno de los meses del año anterior, en este problema nos plantean diferentes resoluciones o problemas a resolver que veremos a continuación:

Para comenzar con el código, incluiremos las siguientes librerías y declaraciones en c++:
```cpp
#include <iostream>
using namespace std;
```
En esta sección, dentro del main, declaramos las siguientes variables:
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
En esta sección del código declaramos las siguientes matrices:
```cpp
int FABRICAS[N];
float VentasMes[N][meses];
```
A continuacion, en la siguiente parte del codigo, se hace una lectura de datos, tanto para las claves de las fábricas como para las ventas por mes de cada fábrica, el cual para leer matrices o vectores bidimensionales se usan ciclos for
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
Para el primer problema que se nos presenta nos indican **encontrar la fabrica que más produjo.**
Para iniciar, creamos nuevas variables y las inicializamos para este problema, donde uno indica el índice y el otro se tomará como un mayor
```cpp
int indiceFabricaMayor = 0;
float mayorProduccion = VentasMes[0][0];
```
Este seria el calculo para llegar a encontrar la fabrica que más produjo en el año, podemos observar que se usa un ciclo for para iterar en la matriz y un if para poder hacer comparaciones y llegar a la fabrica que más produjo en el año
```cpp
for (int i = 1; i < N; i++) {
	for (int j = 1; j < meses; j++) {
		if (VentasMes[i][j] > mayorProduccion) {
			mayorProduccion = VentasMes[i][j];			
			indiceFabricaMayor = i;
		}

	}
}
```
Esta vendría siendo la impresión en pantalla donde muestra la clave de la fábrica que más produjo en el año pasado y cuánto fue lo que produjo
```cpp
cout << "La fábrica que más produjo fue la clave " << FABRICAS[indiceFabricaMayor]
	<< " con una producción de " << mayorProduccion << endl;
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA2MDk3MDQ2Miw0OTc4MTg4MTAsLTYzNT
Q4NDI0NSwxNTA0MzQyNjAwLDc3ODA4NDIzMiwtNjg1NTQ2NzM3
LC0xMjMxNDAwODE1LC0xMzI2NzU2ODAzLC02NzkxODkxMjIsLT
I4MDA2NzQ3NSwtMTYyODkxOTM4NywtNzIzMjk4NzUyLC0xNDI2
ODE1OTE1LC0xOTUxMTIzODI2LC05NTgzNzM5MCwtMTA2ODk0Mj
gwLC0xNzQ2MDI5MjYsLTIwODg3NDY2MTIsMjYzODM2OTA5LDQ3
MDgyNTA3M119
-->