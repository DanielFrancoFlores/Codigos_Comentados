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
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwOTAwMTAyODYsNDk3ODE4ODEwLC02Mz
U0ODQyNDUsMTUwNDM0MjYwMCw3NzgwODQyMzIsLTY4NTU0Njcz
NywtMTIzMTQwMDgxNSwtMTMyNjc1NjgwMywtNjc5MTg5MTIyLC
0yODAwNjc0NzUsLTE2Mjg5MTkzODcsLTcyMzI5ODc1MiwtMTQy
NjgxNTkxNSwtMTk1MTEyMzgyNiwtOTU4MzczOTAsLTEwNjg5ND
I4MCwtMTc0NjAyOTI2LC0yMDg4NzQ2NjEyLDI2MzgzNjkwOSw0
NzA4MjUwNzNdfQ==
-->