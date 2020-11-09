# Práctica 3.3: Comprobación numérica

* Crear un formulario que lea un número, después un mensaje que nos indicará si era realmente un número o no lo es. Si lo fuera, si tiene decimales.

- **Implementación:**
	* **Formulario** `form-practica3.3.php` que cree el formulario con el método GET y envíe los campos a `Lab33.php`. Se debe crear un formulario que tenga el número con posibilidad de hasta 3 decimales y su correspondiente etiqueta.
	* **Programa** `Lab33.php`: debe verificar que se ha recibido el número y verificamos si es un número (is_numeric($n) es una función que verifica si $n es un número) y luego chequea si tiene decimales. Debe de imprimir los mensajes: **Es número entero**, **Es número decimal**, **No se ha recibido un número**. 
