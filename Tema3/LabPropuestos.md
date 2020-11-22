* # Laboratorios Propuestos

  ### Para todos los ejercicios propuestos de formularios, se recomienda utilizar los siguientes links:

  [Formularios y sus etiquetas en Español](https://www.mclibre.org/consultar/htmlcss/html/html-formularios.html)

  [Referencia HTML Mozilla](https://developer.mozilla.org/es/docs/Web/HTML)

  ## Lab3.6: Recogida de Datos I

  * Crea un formulario html con este aspecto:

  ![image-20201122174147309](/home/user22/.config/Typora/typora-user-images/image-20201122174147309.png)

  * El desplegable **Edad** debe tener estas 4 opciones: **menor de 20 años**, **entre 20 y 39 años**, **Entre 40 y 59 años**, **60 o más años**.

  * El formulario tiene dos acciones: **Borrar** que elimina cualquier dato del formulario para volver a escribir nuevos valores y **Enviar** que envía la información a otra página con los datos que recoge del formulario más un enlace para volver al formulario incial vacío.

    

    **Vista del formulario rellenado**

    ![image-20201122174725163](/home/user22/.config/Typora/typora-user-images/image-20201122174725163.png)

    **Vista de la página de impresión de resultados al Enviar la información**

  ![image-20201122174745247](/home/user22/.config/Typora/typora-user-images/image-20201122174745247.png)

  ---

  ## Lab 3.7

  Se tiene el siguiente formulario de **Inserción de vivienda**. El tipo de vivienda es Adosado, Unifamiliar y Piso. Y la zona es Centro o Periferia. Se debe verificar que tanto el precio como el tamaño tengan valor  (recordar que la ausencia de valor es el valor **NULL**) y sean números. Sólo se debe imprimir la información que esté rellenada en otra página. Se realizará el **vivienda.html** que tiene el formulario y el **vivienda.php** que es el que recoge las variables. No es necesario verificar que existen las variables de formulario.


* Caso en que el precio no es un número y el tamaño está vacío.

  

​		![image-20201122202739645](/home/user22/.config/Typora/typora-user-images/image-20201122202739645.png)

Salida al vivienda.php

![image-20201122203020814](/home/user22/.config/Typora/typora-user-images/image-20201122203020814.png)

* Caso en el que todos los valores están creados:

  ![image-20201122202913115](/home/user22/.config/Typora/typora-user-images/image-20201122202913115.png)

  Salida al vivienda.php

![image-20201122202936581](/home/user22/.config/Typora/typora-user-images/image-20201122202936581.png)

* En el caso en el que sólo se rellene el tipo, zona (por defecto ambos), precio y tamaño:

  ![image-20201122203646689](/home/user22/.config/Typora/typora-user-images/image-20201122203646689.png)

## Lab 3.9

Cálculo de IMC. El índice de masa corporal o IMC se calcula con la fórmula: **imc = peso (altura ^ 2)**. Se considera con referente al resultado en los siguientes parámetros:

* imc <= 18.5 : Bajo peso
* 18.5 > imc <= 24.9 : Peso normal
* 24.9 > imc <= 29.9 : Sobrepeso
* imc > 30: Obesidad

Crea un formulario que recoja peso (en kg) y altura (en metros). Que verifique que existen las variables y que sus valores son números. Debe imprimir un mensaje mostrando el IMC y en qué estado está según el mismo.