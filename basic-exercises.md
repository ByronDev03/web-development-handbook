EJERCICIOS BASICOS EN C++

## Ejercicio 1. 
Crear un algoritmo que lea 3 números e imprima el doble y la mitad de los mismos.

<details>
<summary>Código en C++</summary>

```
//Crear un algoritmo que lea 3 números e imprima el doble y la mitad de los mismos.
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


## Ejercicio 2. 
Crear un algoritmo que lea desde teclado 3 números e imprima en pantalla el producto de los números ingresados.

3. Crear un algoritmo que calcule el cuadrado de un número ingresado
desde el teclado.

4. Crear un algoritmo que lea el costo de un producto y obtenga como
resultado el descuento del 15%.

5. Cuál será el costo de un producto si el tendero recibe $4 de ganancia
lo cual es el 25% del costo real.

6. Crear un algoritmo que calcule cuanto pagara una persona por la
compra 3 computadoras si el costo de las computadoras son
diferentes.

7. Cuanto pagara una persona por la compra de un televisor con un
costo de $8,000. Si este tiene un descuento del 10%.

8. Crear un algoritmo que calcule el salario semanal de una persona en
donde el trabajador labora un número variable de días a la semana
y gana $200.00 diarios.

9. Convertir segundos a minutos y horas.

10.Un joven estudia en una escuela particular y la escuela le otorga un
descuento del 35%, solicitar el costo real de la colegiatura e imprimir
en pantalla el descuento y el total a pagar ya con el descuento
aplicado.

11.Una tienda ofrece un descuento del 40% sobre el total de la compra
y un cliente desea saber cuánto deberá pagar finalmente por su
compra y el descuento.

12.Diseñar un algoritmo que lea el valor correspondiente a una distancia
en millas y las escriba expresadas en metros. Sabiendo que 1 milla
equivale a 1852 metros.

13.Diseñar un algoritmo que reciba como entrada una medida
expresada en centímetros la convierta en pulgadas (1pulgada = 2.54
centímetros).

14.Suponga que un individuo desea invertir su capital en un banco y
desea saber cuánto dinero ganara después de un mes, el banco
paga a razón de 2% mensual.

15.Calcular la ganancia de una inversión con un interés del 35% anual
en un periodo de 10 meses.

16.una tienda desea calcular lo siguiente: el monto de la compra, el IVA
(16%), el total (monto más iva) y el cambio del cliente.

17.Suponga que un individuo desea invertir su capital en un banco y
desea saber cuánto dinero tendrá en el banco después de 3 años, el
banco paga a razón de 3% mensual.

18.Un vendedor recibe un sueldo base más un 10% extra por comisión de
sus ventas, el vendedor desea saber cuánto dinero obtendrá por
concepto de comisiones por las tres ventas que realiza en la semana
y el total que recibirá en la semana tomando en cuenta su sueldo
base y comisiones.

19.Un maestro desea saber qué porcentaje de hombres y que
porcentaje de mujeres hay en un grupo de estudiantes, recibiendo
como entrada el número de hombres y mujeres del grupo.

20.Tres personas deciden invertir su dinero para fundar una empresa.
Cada una de ellas invierte una cantidad distinta. Obtener el
porcentaje que cada quien invierte con respecto a la cantidad total
invertida.

21.Una embotelladora de agua ofrece por aniversario un descuento del
25% en compara de agua, si el garrafón de agua tiene un costo de
$12. Calcular el total a pagar por la compra de uno o más garrafones.

22.Calcular la calificación final de juan si esta se compone de los
siguientes porcentajes:
50% del promedio de sus tres calificaciones parciales.
30% examen final.
20% proyecto final.