# Práctica 3.2: Cálculo de salario

* Lee el nombre, los apellidos, el salario (número con decimales) y la edad de una persona ( un número ) en un formulario.
Recoge los datos y con ellos calcula un nuevo salario para esa pesona en base a esta situación:

- Si el salario es mayor de 2000 €, no cambiará.
- Si el salario está entre 1000 y 2000:
	* Si además la edad es mayor de 45 años, se sube un 3%.
	* Si la edad es menor de 45 o igual, se sube un 10%.
- Si el salario es menor de 1000.
	* Los menores de 30 años cobrarán, a partir de ahora, exactamente 1100 €.
	* De 30 a 45 años, sube un 3%.
	* A los mayores de 45 años, sube un 15%.
- **Implementación:**
	* **Formulario** `form-practica.php` que cree el formulario con el método GET y envíe los campos a `Lab32.php`. Se debe crear un formulario que tenga el nombre, apellidos, edad, salario y sus correspondientes etiquetas.
	* **Programa** `Lab32.php` que deberá comprobar que cada una de las variables existen y en ese caso realizar los cálculos de salarios que se indican al principio e imprimirlos en un mensaje: `Nombre Apellidos, tu salario será 1500 euros". En caso de no tener las variables del formulario, se deberá imprimir en HTMl un mensaje que diga **Faltan datos** y redireccionar otra vez a **form-practica.php**. Para redireccionar podemos imprimir un enlace html `<a href="form-practica.php">...</a>` o bien utilizar la función PHP `Redirect ("Location":"form-practica.php");`
