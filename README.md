# Ejecicios_Javascript

1. Mostrar por consola la tabla de multiplicar del 5 utilizando la sentencia for de la siguiente manera:
5 x 0 = 0
5 x 1 = 5
5 x 2 = 10
...

### Solucion
```Javascript
for (var i = 0; i <= 10; i++) {
  var result = 5 * i;
  console.log("5 x " + i + " = " + result);
}
```

2. Modificar el programa anterior y mostrar las 10 tablas de multiplicar.
### Solucion
```Javascript
        for (var i = 0; i <= 10; i++) {
          var result = 1 * i;
          console.log("1 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 2 * i;
          console.log("2 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 3 * i;
          console.log("3 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 4 * i;
          console.log("4 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 5 * i;
          console.log("5 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 6 * i;
          console.log("6 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 7 * i;
          console.log("7 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 8 * i;
          console.log("8 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 9 * i;
          console.log("9 x " + i + " = " + result);
        }

        for (var i = 0; i <= 10; i++) {
          var result = 10 * i;
          console.log("10 x " + i + " = " + result);
        }
```
3. Pedir por pantalla a través de prompt un texto y mostrar en un alert si el texto introducido es un valor numérico o es una cadena.
### Solucion
```Javascript
var texto = prompt("Introduce un texto:");

if (!isNaN(texto)) {
  alert("El texto introducido es un valor numérico.");
} else {
  alert("El texto introducido es una cadena de texto.");
}

```
4. Pedir dos textos por pantalla a través de prompt y mostrar en un alert las dos cadena concatenadas.
### Solucion
```Javascript
// Pedir el primer texto al usuario
var texto1 = prompt("Ingresa el primer texto:");

// Pedir el segundo texto al usuario
var texto2 = prompt("Ingresa el segundo texto:");

// Concatenar las dos cadenas
var resultado = texto1 + texto2;

// Mostrar la concatenación en un alert
alert("El resultado de la concatenación es: " + resultado);
```
5. Pedir dos números por pantalla con prompt y mostrar la suma de ambos.  Se debe validar que los números introducidos sean números.
### Solucion
```Javascript
// Pedir el primer número al usuario
var numero1 = prompt("Ingresa el primer número:");

// Validar si el primer número es válido
if (isNaN(numero1)) {
  alert("El valor ingresado no es un número válido. Por favor, ingresa un número.");
}

// Pedir el segundo número al usuario
var numero2 = prompt("Ingresa el segundo número:");

// Validar si el segundo número es válido
if (isNaN(numero2)) {
  alert("El valor ingresado no es un número válido. Por favor, ingresa un número.");
}

// Convertir los números a tipo Number
numero1 = Number(numero1);
numero2 = Number(numero2);

// Calcular la suma de los números
var suma = numero1 + numero2;

// Mostrar la suma en un alert
alert("La suma de los números ingresados es: " + suma);
```

6. Pedir dos números por pantalla y una operación (+, -, *, /) y mostrar en un alert el resultado de la operación.  Si la operación no es ninguna de las anteriores, se debe mostrar el mensaje "Operación incorrecta".  Se debe validar que los valores introducidos sean números.
### Solucion
```Javascript
var numero1 = prompt("Introduce el primer número:");
var numero2 = prompt("Introduce el segundo número:");
var operacion = prompt("Introduce la operación (+, -, *, /):");

// Validar que los valores introducidos sean números
if (isNaN(numero1) || isNaN(numero2)) {
  alert("Los valores introducidos no son números.");
} else {
  // Realizar la operación correspondiente
  var resultado;
  switch (operacion) {
    case "+":
      resultado = parseFloat(numero1) + parseFloat(numero2);
      break;
    case "-":
      resultado = parseFloat(numero1) - parseFloat(numero2);
      break;
    case "*":
      resultado = parseFloat(numero1) * parseFloat(numero2);
      break;
    case "/":
      resultado = parseFloat(numero1) / parseFloat(numero2);
      break;
    default:
      alert("Operación incorrecta.");
      break;
  }

  // Mostrar el resultado en un alert
  if (resultado !== undefined) {
    alert("El resultado de la operación es: " + resultado);
  }
}

```
7. Leer tres notas de los estudiantes y calcular la media.  Tiene que indicar si está reprobado (nota < 3) o aprobado, junto con la nota media.  Si alguna nota no es un número, no dejar de pedirlas hasta que sea correcta.
### Solucion
```Javascript
// Declarar variables para las notas y la suma
var nota1, nota2, nota3, suma, promedio;

// Pedir la primera nota al usuario y validar que sea un número válido
do {
  nota1 = prompt("Ingresa la primera nota:");
} while (isNaN(nota1));

// Pedir la segunda nota al usuario y validar que sea un número válido
do {
  nota2 = prompt("Ingresa la segunda nota:");
} while (isNaN(nota2));

// Pedir la tercera nota al usuario y validar que sea un número válido
do {
  nota3 = prompt("Ingresa la tercera nota:");
} while (isNaN(nota3));

// Calcular la suma de las notas
suma = parseFloat(nota1) + parseFloat(nota2) + parseFloat(nota3);

// Calcular el promedio
promedio = suma / 3;

// Determinar si el estudiante está aprobado o reprobado
var estado;
if (promedio >= 3) {
  estado = "Aprobado";
} else {
  estado = "Reprobado";
}

// Mostrar el promedio y el estado en un alert
alert("El promedio de las notas es: " + promedio.toFixed(2) + "\nEstado: " + estado);7
```
8. Introducir dos números e indicar cuál es el mayor o si son iguales.
### Solucion
```Javascript
var numero1 = prompt("Introduce el primer número:");
var numero2 = prompt("Introduce el segundo número:");

if (numero1 > numero2) {
  alert("El primer número es mayor que el segundo número.");
} else if (numero1 < numero2) {
  alert("El segundo número es mayor que el primer número.");
} else {
  alert("Los dos números son iguales.");
}

```
9. Pintar un cuadrado de asteriscos de 5 por cada lado
### Solucion
```Javascript
// Declarar una variable para almacenar el tamaño del cuadrado
var lado = 5;

// Declarar una variable para almacenar el cuadrado
var cuadrado = "";

// Construir el cuadrado de asteriscos
for (var i = 0; i < lado; i++) {
  for (var j = 0; j < lado; j++) {
    cuadrado += "* ";
  }
  cuadrado += "\n";
}

// Mostrar el cuadrado en la consola
console.log(cuadrado);
```
10. Cree esta figura por pantalla con JS
       *
     ***
   *****
 *******
********
 *******
   *****
     ***
      *
### Solucion
```Javascript
var n = 5; // Número de filas de la figura
var figura = ""; // Variable para almacenar la figura

// Bucle para crear las filas superiores de la figura
for (var i = 1; i <= n; i++) {
  // Añadir espacios en blanco antes de los asteriscos
  for (var j = 1; j <= n - i; j++) {
    figura += " ";
  }

  // Añadir los asteriscos
  for (var k = 1; k <= 2 * i - 1; k++) {
    figura += "*";
  }

  figura += "\n"; // Salto de línea
}

// Bucle para crear las filas inferiores de la figura
for (var i = n - 1; i >= 1; i--) {
  // Añadir espacios en blanco antes de los asteriscos
  for (var j = 1; j <= n - i; j++) {
    figura += " ";
  }

  // Añadir los asteriscos
  for (var k = 1; k <= 2 * i - 1; k++) {
    figura += "*";
  }

  figura += "\n"; // Salto de línea
}

console.log(figura); // Mostrar la figura por consola
```