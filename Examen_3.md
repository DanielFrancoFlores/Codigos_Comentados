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

```cpp
int FABRICAS[N]; 
float VentasMes[N][meses];
 ```
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTE2MzQwMDg1LC0xMDY4OTQyODAsLTE3ND
YwMjkyNiwtMjA4ODc0NjYxMiwyNjM4MzY5MDksNDcwODI1MDcz
LC0zMzI0NTUzNjNdfQ==
-->