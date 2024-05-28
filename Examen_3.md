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
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgzODE1MDczMyw0OTc4MTg4MTAsLTYzNT
Q4NDI0NSwxNTA0MzQyNjAwLDc3ODA4NDIzMiwtNjg1NTQ2NzM3
LC0xMjMxNDAwODE1LC0xMzI2NzU2ODAzLC02NzkxODkxMjIsLT
I4MDA2NzQ3NSwtMTYyODkxOTM4NywtNzIzMjk4NzUyLC0xNDI2
ODE1OTE1LC0xOTUxMTIzODI2LC05NTgzNzM5MCwtMTA2ODk0Mj
gwLC0xNzQ2MDI5MjYsLTIwODg3NDY2MTIsMjYzODM2OTA5LDQ3
MDgyNTA3M119
-->