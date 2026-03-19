<h1 align="center">EJERCICIOS BÁSICOS</h1>

---

##### Ejercicio 1. Crear un algoritmo que lea 3 números e imprima el doble y la mitad de los mismos
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_1
	Definir ResSuma, ResDoble, ResMitad, Num1, Num2, Num3 Como Entero
	ResSuma <- 0;
	ResDoble <- 0;
	ResMitad <- 0;
	Num1 <- 0;
	Num2 <- 0;
	Num3 <- 0;
	
	Escribir "------PROGRAMA QUE CALCULA EL DOBLE Y LA MITAD DE 3 NUMEROS INGRESADOS------";
	Escribir "Ingrese el primer número: ";
	Leer Num1;
	Escribir "Ingrese el segundo número: ";
	Leer Num2;
	Escribir "Ingrese el tercer número: ";
	Leer Num3;
	
	ResSuma <- Num1+Num2+Num3;
	ResDoble <- ResSuma*2;
	ResMitad <- ResDoble/2;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El doble de los 3 números es: ",ResDoble;
	Escribir "La mitad de los 3 números es: ",ResMitad;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int num1 = 0, num2 = 0, num3 = 0;
int suma = 0, doble = 0;
float mitad = 0;
void resultados()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"SUMA: "<<suma<<endl;
	cout<<"DOBLE: "<<doble<<endl;
	cout<<"MITAD: "<<mitad<<endl;
}
void DobMit()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL DOBLE Y LA MITAD DE 3 NUMEROS INGRESADOS---"<<endl;
	cout<<"Ingrese el numero 1: ";
	cin>>num1;
	cout<<"Ingrese el numero 2: ";
	cin>>num2;
	cout<<"Ingrese el numero 3: ";
	cin>>num3;
	
	suma = num1 + num2 + num3;
	doble = suma * 2;
	mitad = doble / 2;
	resultados();
}
int main()
{
	system("color 0A");
	DobMit();
	return 0;
}
```
</details>

##### Ejercicio 2. Crear un algoritmo que lea desde teclado 3 números e imprima en pantalla el producto de los números ingresados
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_2
	Definir Num1,Num2,Num3,Resultado Como Entero
	Resultado <- 0;
	Num1 <- 0;
	Num2 <- 0;
	Num3 <- 0;
	
	Escribir "------PROGRAMA QUE LEE Y MUESTRA EL PRODUCTO DE 3 NUMEROS INGRESADOS------";
	Escribir "Ingrese el primer número: ";
	Leer Num1;
	Escribir "Ingrese el segundo número: ";
	Leer Num2;
	Escribir "Ingrese el tercer número: ";
	Leer Num3;
	
	Resultado <- Num1*Num2*Num3; 
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El producto de 3 números ingresados es: ",Resultado;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int num1 = 0, num2 = 0, num3 = 0, prdt = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL PRODUCTO ES: "<<prdt;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE LEE Y MUESTRA EL PRODUCTO DE 3 NUMEROS INGRESADOS---"<<endl;
	cout<<"Ingrese el numero 1: ";
	cin>>num1;
	cout<<"Ingrese el numero 2: ";
	cin>>num2;
	cout<<"Ingrese el numero 3: ";
	cin>>num3;
}
void CalPrdt()
{
	EntradaDatos();
	prdt = num1 * num2 * num3;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalPrdt();
	return 0;
}
```
</details>

##### Ejercicio 3. Crear un algoritmo que calcule el cuadrado de un número ingresado desde el teclado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_3
	Definir Num, ResCuad Como Entero
	ResCuad <- 0;
	Num <- 0;
	
	Escribir "------PROGRAMA QUE CALCULA EL CUADRADO DE UN NUMERO INGRESADO------";
	Escribir "Ingrese un número: ";
	Leer Num;
	
	ResCuad <- Num * Num;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El cuadrado del numero ", Num , " es: ", ResCuad;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int num = 0, ResCuad = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL CUADRADO DEL NUMERO "<<num<<" ES: "<<ResCuad;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL CUADRADO DE UN NUMERO INGRESADO---"<<endl;
	cout<<"Ingrese un numero: ";
	cin>>num;
}
void CalCuad()
{
	EntradaDatos();
	ResCuad = num * num;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalCuad();
	return 0;
}
```
</details>

##### Ejercicio 4. Crear un algoritmo que lea el costo de un producto y obtenga como resultado el descuento del 15%
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_4
	Definir Costo Como Entero
	Definir Descuento Como Real
	Costo <- 0;
	Descuento <- 0;
	
	Escribir "------PROGRAMA QUE OBTENGA EL DESCUENTO DEL 15% DE UN PRODUCTO INGRESADO-----";
	Escribir "Ingrese el costo del producto: ";
	Leer Costo
	
	Descuento <- Costo * 0.15;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El descuento del producto es de: $",Descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int costo = 0;
float descuento = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"El descuento del producto es de: $"<<descuento;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE OBTIENE EL DESCUENTO DEL 15% DE UN PRODUCTO INGRESADO---"<<endl;
	cout<<"Ingrese el costo del producto: ";
	cin>>costo;
}
void CalCosto()
{
	EntradaDatos();
	descuento = costo * 0.15;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalCosto();
	return 0;
}
```
</details>

##### Ejercicio 5. ¿Cuál será el costo de un producto si el tiendero recibe $4 de ganancia lo cual es el 25% del costo real?
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_5
	Definir costo Como Entero
	costo <- 0;
	
	Escribir "------PROGRAMA QUE CALCULE EL COSTO DE UN PRODUCTO------";
	
	costo <- 100*4/25;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El costo del producto es de: $",costo;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
float costo = 0;
void ImprimirDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULE EL COSTO DE UN PRODUCTO---"<<endl;
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL COSTO DEL PRODUCTO ES DE: $"<<costo;
}
void CalCosto()
{
	costo = 100 * 4 / 25;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalCosto();
	return 0;
}
```
</details>

##### Ejercicio 6. Crear un algoritmo que calcule cuanto pagara una persona por la compra 3 computadoras si el costo de las computadoras son diferentes
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_6
	Definir PreCom1, PreCom2, PreCom3, total Como Entero
	PreCom1 <- 0;
	PreCom2 <- 0;
	PreCom3 <- 0;
	total <- 0;
	
	Escribir "------PROGRAMA QUE CALCULA CUANTO SE DEBE DE PAGAR POR 3 COMPUTADORAS------";
	Escribir "Ingrese el precio de la primer computadora: ";
	Leer PreCom1;
	Escribir "Ingrese el precio de la segunda computadora: ";
	Leer PreCom2;
	Escribir "Ingrese el precio de la tercera computadora: ";
	Leer PreCom3;
	
	total <- (PreCom1*PreCom2*PreCom3)/3;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total a pagar por las 3 computadoras es de: $",total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int PreCom1 = 0, PreCom2 = 0, PreCom3 = 0, subtotal = 0;
float total = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL TOTAL POR 3 COMPUTADORAS ES DE: $"<<total;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA CUANTO SE DEBE DE PAGAR POR 3 COMPUTADORAS---"<<endl;
	cout<<"Ingrese el precio de la computadora 1: $";
	cin>>PreCom1;
	cout<<"Ingrese el precio de la computadora 2: $";
	cin>>PreCom2;
	cout<<"Ingrese el precio de la computadora 3: $";
	cin>>PreCom3;
}
void CostoPC()
{
	EntradaDatos();
	subtotal = PreCom1 * PreCom2 * PreCom3;
	total = subtotal / 3;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CostoPC();
	return 0;
}
```
</details>

##### Ejercicio 7. ¿Cuanto pagara una persona por la compra de un televisor con un costo de $8,000. Si este tiene un descuento del 10%?
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_7
	Definir  Precio, PagoTotal, Descuento Como Entero
	Precio <- 0;
	PagoTotal <- 0;
	Descuento <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULA LA COMPRA DE UN TELEVISOR DE $8,000-----";
	Escribir "Ingrese el precio del televisor: ";
	Leer Precio;
	
	Descuento <- Precio * 0.10;
	PagoTotal <- Precio - Descuento;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "Lo que se tendra que pagar es de: $",PagoTotal;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<stdlib.h>
using namespace std;
int descuento = 0;
float PagoTotal = 0;
void ImprimirDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA LA COMPRA DE UN TELEVISOR DE $8,000---"<<endl;
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"PAGO CON DESCUENTO APLICADO ES DE: $"<<PagoTotal;
}
void CalPago()
{
	descuento = 8000 * 0.10;
	PagoTotal = 8000 - descuento; 
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalPago();
	return 0;
}
```
</details>

##### Ejercicio 8. Crear un algoritmo que calcule el salario semanal de una persona en donde el trabajador labora un número variable de días a la semana y gana $200.00 diarios
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_8
	Definir Diastrab, Total_dias, Total_salario Como Entero
	Diastrab <- 0;
	Total_dias <- 0;
	Total_salario <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE EL SALARIO SEMANAL DE UN TRABAJADOR-----";
	Escribir "Ingrese la cantidad de dias trabajados a la semana: ";
	Leer Diastrab;
	
	Total_dias <- Diastrab * 200;
	Total_salario <- Total_dias / 5; 
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "Por ", Diastrab , " dias trabajados a la semana su salario es de: $",Total_salario; 
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int DiasTrab = 0, TotalDias = 0, TotalSalario = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"POR "<<DiasTrab<<" DIAS TRABAJADOS A LA SEMANA SU SALARIO ES DE: $"<<TotalSalario;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL SALARIO SEMANAL DE UN TRABAJADOR---"<<endl;
	cout<<"Ingrese los dias trabajados a la semana: ";
	cin>>DiasTrab;
}
void SalarioPersona()
{
	EntradaDatos();
	TotalDias = DiasTrab * 200;
	TotalSalario = TotalDias / 5;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	SalarioPersona();
	return 0;
}
```
</details>

##### Ejercicio 9. Convertir segundos a minutos y horas
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_9
	Definir Seg, Min, Hrs Como Entero
	Seg <- 0;
	Min <- 0;
	Hrs <- 0;
	
	Escribir "------PROGRAMA QUE CONVIERTA SEGUNDOS A MINUTOS Y HORAS------";
	Escribir "Ingrese la cantidad de segundos a convertir: ";
	Leer Seg;
	
	Min <- Seg/60;
	Hrs <- Seg/3600;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "Minutos: ",Min;
	Escribir "Horas: ",Hrs;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int seg = 0, mins = 0, hrs = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"MINUTOS: "<<mins<<endl;
	cout<<"HORAS: "<<hrs<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CONVIERTA SEGUNDOS A MINUTOS Y HORAS---"<<endl;
	cout<<"Ingrese los segundos a convertir: ";
	cin>>seg;	
}
void SegMinHrs()
{
	EntradaDatos();
	mins = seg / 60;
	hrs = seg / 3600;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	SegMinHrs();
	return 0;
}
```
</details>

##### Ejercicio 10. Un joven estudia en una escuela particular y la escuela le otorga un descuento del 35%, solicitar el costo real de la colegiatura e imprimir en pantalla el descuento y el total a pagar ya con el descuento aplicado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_10
	Definir Costo_cole, Descuento, Total_pagar Como Entero;
	Costo_cole <-0;
	Descuento <- 0;
	Total_pagar <- 0;
	
	Escribir "Ingrese el costo real de la colegiatura: ";
	Leer Costo_cole;
	
	Descuento <- Costo_cole * 0.35;
	Total_pagar <- Costo_cole - Descuento;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El descuento aplicado es de: $",Descuento;
	Escribir "El total a pagar con el descuento aplicado: $",Total_pagar;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int CostoCole = 0, descuento = 0, TotalPagar = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"DESCUENTO APLICADO: $"<<descuento<<endl;
	cout<<"TOTAL A PAGAR CON DESCUENTO APLICADO: $"<<TotalPagar<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL DESCUENTO Y EL TOTAL A PAGAR DE UNA COLEGIATURA---"<<endl;
	cout<<"Ingrese el costo de la colegiatura: $";
	cin>>CostoCole;
}
void PagoColegiatura()
{
	EntradaDatos();
	descuento = CostoCole * 0.35;
	TotalPagar = descuento - CostoCole;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	PagoColegiatura();
	return 0;
}
```
</details>

##### Ejercicio 11. Una tienda ofrece un descuento del 40% sobre el total de la compra y un cliente desea saber cuánto deberá pagar finalmente por su compra y el descuento.
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_11
	Definir Total_compra, Descuento, Total_pago Como Entero 
	Total_compra <- 0;
	Descuento <- 0;
	Total_pago <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULA EL TOTAL DE UNA COMPRA Y SU DESCUENTO-----";
	Escribir "Ingrese el total de la compra: ";
	Leer Total_compra;
	
	Descuento <- Total_compra * 0.40;
	Total_pago <- Total_compra - Descuento;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total a pagar es de: $",Total_pago;
	Escribir "Aplicando el descuento seria de: $",Descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int TotalCompra = 0, Descuento = 0, TotalPago = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"TOTAL A PAGAR: $"<<TotalPago<<endl;
	cout<<"DESCUENTO APLICADO: $"<<Descuento<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL TOTAL DE UNA COMPRA Y SU DESCUENTO---"<<endl;
	cout<<"Ingrese el total de la compra: $";
	cin>>TotalCompra;
}
void PagoTienda()
{
	EntradaDatos();
	Descuento = TotalCompra * 0.40;
	TotalPago = Descuento - TotalCompra;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	PagoTienda();
	return 0;
}
```
</details>

##### Ejercicio 12. Diseñar un algoritmo que lea el valor correspondiente a una distancia en millas y las escriba expresadas en metros. Sabiendo que 1 milla equivale a 1852 metros
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_12
	Definir DistMillas, Mtrs Como Entero
	DistMillas <- 0;
	Mtrs <-0;
	
	Escribir "------PROGRAMA QUE CONVIERTA MILLAS A METROS------";
	Escribir "Ingrese la distancia en millas: ";
	Leer DistMillas;
	
	Mtrs <- DistMillas * 1852;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "Las ", DistMillas ," millas ingresadas da como conversion a metros de: ", Mtrs ," Mtrs";
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int DistMillas = 0, Mtrs = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LAS "<<DistMillas<<" MILLAS A METROS SON: "<<Mtrs<<" Mtrs"; 
} 
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CONVIERTE MILLAS A METROS---"<<endl;
	cout<<"Ingrese la distancia en millas: ";
	cin>>DistMillas;
}
void MillasMtrs()
{
	EntradaDatos();
	Mtrs = DistMillas * 1852;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	MillasMtrs();
	return 0;
}
```
</details>

##### Ejercicio 13. Diseñar un algoritmo que reciba como entrada una medida expresada en centímetros la convierta en pulgadas (1 pulgada = 2.54 centímetros)
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_13
	Definir Centimetros Como Entero
	Definir Pulgadas Como Real
	Centimetros <- 0;
	Pulgadas <- 0;
	
	Escribir "-----PROGRAMA QUE CONVIERTA CENTIMETROS A PULGADAS-----";
	Escribir "Ingrese los centimetros a convertir: ";
	Leer  Centimetros;
	
	Pulgadas <- Centimetros / 2.54;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "Los ", Centimetros , " centimetros convertidos a pulgadas da: ",Pulgadas;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int cms = 0;
float Pulgadas = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LOS "<<cms<<" CENTIMETROS A PULGADAS ES DE: "<<Pulgadas;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CONVIERTE CENTIMETROS A PULGADAS---"<<endl;
	cout<<"Ingrese los centimetros a convertir: ";
	cin>>cms;
}
void CentPulg()
{
	EntradaDatos();
	Pulgadas = cms / 2.54;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CentPulg();
	return 0;
}
```
</details>

##### Ejercicio 14. Suponga que un individuo desea invertir su capital en un banco y desea saber cuánto dinero ganara después de un mes, el banco paga a razón de 2% mensual
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_14
	Definir Capital, Ganancia Como Entero
	Capital <- 0;
	Ganancia <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE LA GANANCIA DE UN INDIVIDUO-----";
	Escribir "Ingrese la capital que desea invertir: ";
	Leer Capital;
	
	Ganancia <- Capital * 0.02;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El cantidad de ", Capital ," ingresada dara como ganancia: $", Ganancia;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int Capital = 0,Ganancia = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LA CAPITAL DE "<<Capital<<" INGRESADA DARA COMO GANANCIA: $"<<Ganancia;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA LA GANANCIA DE UN INDIVIDUO---"<<endl;
	cout<<"Ingrese la capital que desea invertir: $";
	cin>>Capital;
}
void CalcGanancia()
{
	EntradaDatos();
	Ganancia = Capital * 0.02;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalcGanancia();
	return 0;
}
```
</details>

##### Ejercicio 15. Calcular la ganancia de una inversión con un interés del 35% anual en un periodo de 10 meses
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_15
	Definir interes, inversion Como Entero	
	Definir Total_ganancia Como Real
	interes <- 0;
	inversion <- 0;
	Total_ganancia <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE LA GANANCIA DE UNA INVERSION-----";
	Escribir "Ingrese el monto de la inversion: ";
	Leer inversion;
	
	interes <- inversion * 0.35;
	Total_ganancia <- interes / 10;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La ganancia obtenida es de: $", Total_ganancia;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int interes = 0, inversion = 0;
float TotalGanancia = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"GANANCIA OBTENIDA: $"<<TotalGanancia;	
} 
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULE LA GANACIA DE UNA INVERSIÓN---"<<endl;
	cout<<"Ingrese el monto de la inversion: $";
	cin>>inversion;	
}
void CalcGanancia()
{
	EntradaDatos();
	interes = inversion * 0.35;
	TotalGanancia = interes / 10;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalcGanancia();
	return 0;
}
```
</details>

##### Ejercicio 16. Una tienda desea calcular lo siguiente: el monto de la compra, el IVA (16%), el total (monto más iva) y el cambio del cliente
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_16
	Definir iva, precio_prdct, pago_prdct, monto_iva, cambio Como Entero
	iva <- 0;
	precio_prdct <- 0;
	pago_prdct <- 0;
	monto_iva <- 0;
	cambio <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE EL MONTO DE LA COMPRA,IVA Y EL CAMBIO-----";
	Escribir "Ingrese el precio del producto: ";
	Leer precio_prdct; 
	Escribir "Ingrese el pago: ";
	Leer pago_prdct;
	
	iva = precio_prdct * 0.16;
	monto_iva = precio_prdct + iva;
	cambio = precio_prdct - pago_prdct;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El iva a pagar es de: $",iva;
	Escribir "El total a pagar ya con el iva incluido es de: $",monto_iva;
	Escribir "Su cambio es de: $", cambio;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
double iva = 0, PrecioPrdct = 0, PagoPrdct = 0;
double total = 0, Cambio = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL IVA A PAGAR ES DE: $"<<iva<<endl;
	cout<<"EL TOTAL A PAGAR CON EL IVA INCLUIDO ES DE: $"<<total<<endl;
	cout<<"SU CAMBIO ES DE: $"<<Cambio<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL MONTO DE LA COMPRA, IVA Y EL CAMBIO---"<<endl;
	cout<<"Ingrese el precio del producto: ";
	cin>> PrecioPrdct;
	cout<<"Ingrese el pago: ";
	cin>> PagoPrdct;
}
void CalIVA()
{
	EntradaDatos();
	iva = PrecioPrdct * 0.16;
	total = PrecioPrdct + iva;
	Cambio = total - PagoPrdct;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalIVA();
	return 0;
}
```
</details>

##### Ejercicio 17. Suponga que un individuo desea invertir su capital en un banco y desea saber cuánto dinero tendrá en el banco después de 3 años, el banco paga a razón de 3% mensual
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_17
	Definir Cant_cap, Inver_total, Pago_banco Como Entero
	Cant_cap <- 0;
	Pago_banco <- 0;
	Inver_total <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE LA CANTIDAD DE DINERO QUE TENDRA UN BANCO EN 3 AÑOS-----";
	Escribir "Ingrese la cantidad de capital que desea invertir: ";
	Leer Cant_cap;
	
	Pago_banco <- Cant_cap * 0.03;
	Inver_total <- Pago_banco / 3;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La cantidad de capital invertida despues de 3 años sera de: $", Inver_total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int CantCap = 0, PagoBanco = 0, InverTotal = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"CAPITAL INVERTIDA: $"<<InverTotal;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA LA CANTIDAD DE DINERO QUE TENDRA UN BANCO EN 3 A�OS---"<<endl;
	cout<<"Ingrese la capital a invertir: $";
	cin>>CantCap;
}
void CalCapital()
{
	EntradaDatos();
	PagoBanco = CantCap * 0.03;
    InverTotal = PagoBanco / 3;	
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalCapital();
	return 0;
}
```
</details>

##### Ejercicio 18. Un vendedor recibe un sueldo base más un 10% extra por comisión de sus ventas, el vendedor desea saber cuánto dinero obtendrá por concepto de comisiones por las tres ventas que realiza en la semana y el total que recibirá en la semana tomando en cuenta su sueldo base y comisiones
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_18
	Definir Sb, Venta1, Venta2, Venta3, Total_ven, Total_pago, Com Como Entero
	Sb <- 0;
	Venta1 <- 0;
	Venta2 <- 0;
	Venta3 <- 0;
	Total_ven <- 0;
        Total_pag <- 0; 
	Com <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE LAS COMISIONES Y EL PAGO TOTAL DE UN VENDEDOR-----";
	Escribir "Ingrese su sueldo base: ";
	Leer Sb;
	Escribir "Ingrese la cantidad de lo que se obtuvo en la venta 1: ";
	Leer Venta1;
	Escribir "Ingrese la cantidad de lo que se obtuvo en la venta 2:";
	Leer Venta2;
	Escribir "Ingrese la cantidad de lo que se obtuvo en la venta 3:";
	Leer Venta3;
	
	Total_ven <- Venta1+Venta2+Venta3;
	Com <- Total_ven*0.10;
	Total_pago <- Sb+Com;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "Su sueldo base ingresado es: $", Sb , " para dar como pago total: $", Total_pago;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int Sb = 0, Venta1 = 0, Venta2 = 0, Venta3 = 0, TotalVenta = 0;
float TotalPago = 0, Com = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"SU COMISION ES: $"<<Com<<endl;
	cout<<"EL TOTAL A PAGAR: $"<<TotalPago<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA LAS COMISIONES Y EL PAGO TOTAL DE UN VENDEDOR---"<<endl;
	cout<<"Ingrese su sueldo base: $";
	cin>>Sb;
	cout<<"Ingrese lo obtenido de la venta 1: $";
	cin>>Venta1;
	cout<<"Ingrese lo obtenido de la venta 2: $";
	cin>>Venta2;
	cout<<"Ingrese lo obtenido de la venta 3: $";
	cin>>Venta3;
}
void CalComPt()
{
	EntradaDatos();
	TotalVenta = Venta1 + Venta2 + Venta3;
	Com = TotalVenta * 0.10;
	TotalPago = Sb + Com; 
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalComPt();
	return 0;
}
```
</details>

##### Ejercicio 19. Un maestro desea saber qué porcentaje de hombres y que porcentaje de mujeres hay en un grupo de estudiantes, recibiendo como entrada el número de hombres y mujeres del grupo
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_19
	Definir  hombres, mujeres , resultado Como Entero
	Hombres <- 0;
	Mujeres <- 0;
	Resultado <-0;	
	
	Escribir "----PROGRAMA QUE CALCULA EL PORCENTAJE DE HOMBRES Y MUJERES QUE HAY EN UN GRUPO DE ESTUDIANTES----";
	Escribir "Ingrese la cantidad de hombres: ";
	Leer hombres;
	Escribir "Ingrese la cantidad de mujeres: ";
	Leer mujeres;
	
	Resultado <- Hombres + Mujeres;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El porcentaje de hombres es de: ",(hombres / resultado) * 100, " %";
	Escribir "El porcentaje de mujeres es de: ",(mujeres / resultado) * 100, " %";
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
float hmrs = 0, mjrs = 0, TotalAlum = 0;
int PorcenHom = 0, PorcenMuj = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"PORCENTAJE HOMBRES: "<<PorcenHom<<"%"<<endl;
	cout<<"PORCENTAJE MUJERES: "<<PorcenMuj<<"%"<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA EL PORCENTAJE DE HOMBRES Y MUJERES QUE HAY EN UN GRUPO DE ESTUDIANTES---"<<endl;
	cout<<"Ingrese la cantidad de hombres: ";
	cin>>hmrs;
	cout<<"Ingrese la cantidad de mujeres: ";
	cin>>mjrs;
}
void PorcenHomMuj()
{
	EntradaDatos();
	TotalAlum = hmrs + mjrs;
	PorcenHom = (hmrs / TotalAlum) * 100;
	PorcenMuj = (mjrs / TotalAlum) * 100;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	PorcenHomMuj();
	return 0;
}
```
</details>

##### Ejercicio 20. Tres personas deciden invertir su dinero para fundar una empresa. Cada una de ellas invierte una cantidad distinta. Obtener el porcentaje que cada quien invierte con respecto a la cantidad total invertida
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_20
	Definir Socio1, Socio2, Socio3, Porcensocio1, Porcensocio2, Porcensocio3, total Como Entero
	Socio1 <- 0;
	Socio2 <- 0;
	Socio3 <- 0;
	Porcensocio1 <- 0;
	Porcensocio2 <- 0;
	Porcensocio3 <- 0;
	total <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE EL PORCENTAJE DE INVERSION-----";
	Escribir "Ingrese lo que el primer socio invirtio: ";
	Leer Socio1;
	Escribir "Ingrese lo que el segundo socio invirtio: ";
	Leer Socio2;
	Escribir "Ingrese lo que el tercer socio invirtio: ";
	Leer Socio3;
	
	total <- Socio1+Socio2+Socio3;
	Porcensocio1 <- Socio1*100/total;
	Porcensocio2 <- Socio2*100/total;
	Porcensocio3 <- Socio3*100/total;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La primera persona invierte el: ", Porcensocio1, " %";
	Escribir "La segunda persona invierte el: ", Porcensocio2, " %";
	Escribir "La tercera persona invierte el: ", Porcensocio3, " %";
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int Socio1 = 0, Socio2 = 0, Socio3 = 0;
int PorcenSocio1 = 0, PorcenSocio2 = 0, PorcenSocio3 = 0, total = 0; 
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LA PRIMERA PERSONA INVIERTE EL: "<<PorcenSocio1<<"%"<<endl;
	cout<<"LA SEGUNDA PERSONA INVIERTE EL: "<<PorcenSocio2<<"%"<<endl;
	cout<<"LA TERCERA PERSONA INVIERTE EL: "<<PorcenSocio3<<"%"<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULE EL PORCENTAJE DE INVERSION---"<<endl;
	cout<<"Ingrese la inversion del primer socio: $";
	cin>>Socio1;
	cout<<"Ingrese la inversion del segundo socio: $";
	cin>>Socio2;
	cout<<"Ingrese la inversion del tercer socio: $";
	cin>>Socio3;
}
void CalcInvers()
{
	EntradaDatos();
	total = Socio1 + Socio2 + Socio3;
	PorcenSocio1 = (Socio1 * 100)/ total;
	PorcenSocio2 = (Socio2 * 100) / total;
	PorcenSocio3 = (Socio3 * 100) / total;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalcInvers();
	return 0;	
}
```
</details>

##### Ejercicio 21. Una embotelladora de agua ofrece por aniversario un descuento del 25% en compara de agua, si el garrafón de agua tiene un costo de $12. Calcular el total a pagar por la compra de uno o más garrafones
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_21
	Definir Descuento, PagoTotal, NumGarrafones, Subtotal Como Entero
	Descuento <- 0;
	PagoTotal <- 0;
	NumGarrafones <- 0;
	Subtotal <- 0;
	
	Escribir "-----PROGRAMA QUE CALCULE EL TOTAL POR LA COMPRA DE GARRAFONES-----";
	Escribir "Ingrese la cantidad de garrafones que desea comprar: ";
	Leer NumGarrafones;
	
	Subtotal <- NumGarrafones*12;
	Descuento <- Subtotal*0.25;
	PagoTotal <- Subtotal - Descuento;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total a pagar por ", NumGarrafones , " garrafones es de: $", PagoTotal;
	Escribir "Con el descuento aplicado: $",Descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int NumGarrafones = 0;
float Descuento = 0, PagoTotal = 0, Subtotal = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"TOTAL A PAGAR POR "<<NumGarrafones<<" GARRAFONES ES DE: $"<<PagoTotal<<endl;
	cout<<"CON EL DESCUENTO APLICADO: $"<<Descuento<<endl;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULE EL TOTAL POR LA COMPRA DE GARRAFONES---"<<endl;
	cout<<"Ingrese la cantidad de garrafones que desea comprar: ";
	cin>>NumGarrafones;
}
void CalcPagoGarrafones()
{
	EntradaDatos();
	Subtotal = NumGarrafones * 12;
	Descuento = Subtotal * 0.25;
	PagoTotal = Subtotal - Descuento;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalcPagoGarrafones();
	return 0;
}
```
</details>

##### Ejercicio 22. Calcular la calificación final de juan si esta se compone de los siguientes porcentajes:
- 50% del promedio de sus tres calificaciones parciales
- 30% examen final
- 20% proyecto final
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_22
	Definir Calpar1, Calpar2, Calpar3, Examfin, Trabfin, Porcenparcial, Porcentrabfin, Calfin Como Entero
	Definir Promedio,Porcenexamfin Como Real
	Calpar1 <- 0;
	Calpar2 <- 0;
	Calpar3 <- 0;
	Examfin <- 0;
	Trabfin <- 0;
	Promedio <- 0;
	Porcenparcial <- 0;
	Porcenexamfin <- 0;
	Porcentrabfin <- 0;
	Calfin <- 0;

	Escribir "-----PROGRAMA QUE CALCULE LA CALIFICACION DE JUAN-----";
	Escribir "Ingrese la primer calificacion parcial que obtuvo: ";
	Leer Calpar1;
	Escribir "Ingrese la segunda calificacion parcial que obtuvo: ";
	Leer Calpar2;
	Escribir "Ingrese la tercera calificacion parcial que obtuvo: ";
	Leer Calpar3;
	Escribir "Ingrese la calificacion que obtuvo en el examen final: "
	Leer Examfin
	Escribir "Ingrese la calificacion que obtuvo en el trabajo final: "
	Leer Trabfin;

	Promedio <- (Calpar1+Calpar2+Calpar3)/3;
	Porcenparcial <- Promedio*0.50;
	Porcenexamfin <- Examfin*0.30;
	Porcentrabfin <- Trabfin*0.20;
	Calfin <- Porcenparcial+Porcenexamfin+Porcentrabfin;
	
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La calificacion final obtenida es de: ",Calfin;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
#include<windows.h>
#include<stdlib.h>
using namespace std;
int Calpar1 = 0, Calpar2 = 0, Calpar3 = 0, Examfin = 0;
int Trabfin = 0, Porcenparcial = 0, Porcentrabfin = 0, Calfin = 0;
float promedio = 0, Porcenexamfin = 0;
void ImprimirDatos()
{
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"CALIFICACION FINAL: "<<Calfin;
}
void EntradaDatos()
{
	cout<<"\t---PROGRAMA QUE CALCULA LA CALIFICACI�N FINAL---"<<endl;
	cout<<"Ingrese la primer calificacion parcial que obtuvo: ";
	cin>>Calpar1;
	cout<<"Ingrese la segunda calificacion parcial que obtuvo: ";
	cin>>Calpar2;
	cout<<"Ingrese la tercer calificacion parcial que obtuvo: ";
	cin>>Calpar3;
	cout<<"Ingrese la calificacion que obtuvo en el examen final: ";
	cin>>Examfin;
	cout<<"Ingrese la calificacion que obtuvo en el trabajo final: ";
	cin>>Trabfin;
	
}
void CalcCaliFinal()
{
	EntradaDatos();
	promedio = (Calpar1 + Calpar2 + Calpar3) / 3;
	Porcenparcial = promedio * 0.50;
	Porcenexamfin = Examfin * 0.30;
	Porcentrabfin = Trabfin * 0.20;
	Calfin = Porcenparcial + Porcenexamfin + Porcentrabfin;
	ImprimirDatos();
}
int main()
{
	system("color 0A");
	CalcCaliFinal();
	return 0;
}
```
</details>