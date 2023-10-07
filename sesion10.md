<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 10

<!-- Su documentación aquí -->

# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno.

# Solucion

### Calcular la cantidad de materiales necesarios para construir una pared de ladrillos

Cálculo de la cantidad de materiales para la construcción: Este ejercicio consiste en calcular la cantidad de materiales necesarios para construir una estructura. Para ello, se debe tener en cuenta las dimensiones de la estructura y la cantidad de materiales necesarios por unidad de área o de volumen. Algunos ejemplos de cálculos de materiales son el cálculo de la cantidad de ladrillos necesarios para construir una pared, o el cálculo de la cantidad de concreto necesario para una losa o columna.

Ejemplo en Java de cómo calcular la cantidad de materiales necesarios para construir una pared de ladrillos:

```java
import java.util.Scanner;

public class CantidadLadrillos {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;

      // Solicita las dimensiones de la pared
      System.out.print("Ingrese el largo de la pared en metros: ");
      largo = input.nextDouble();
      System.out.print("Ingrese el alto de la pared en metros: ");
      alto = input.nextDouble();
      System.out.print("Ingrese el ancho de la pared en metros: ");
      ancho = input.nextDouble();

      // Solicita las dimensiones del ladrillo
      System.out.print("Ingrese el largo del ladrillo en metros: ");
      largoLadrillo = input.nextDouble();
      System.out.print("Ingrese el alto del ladrillo en metros: ");
      altoLadrillo = input.nextDouble();
      System.out.print("Ingrese el ancho del ladrillo en metros: ");
      anchoLadrillo = input.nextDouble();

      // Calcula el área de la pared y del ladrillo
      double areaPared = largo * alto;
      double areaLadrillo = largoLadrillo * altoLadrillo;

      // Calcula la cantidad de ladrillos necesarios
      cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));

      // Muestra el resultado en la consola
      System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);
   }
}
```

# Explicacion del ejercicio de calcular la cantidad de materiales necesarios para construir una pared de ladrillos:

Para este ejemplo se trabaja en el metodo main no hay necesdiad de crear mas metodos:

- Lo primero es crear el proyecto con la clase que se llama cantidadLadrillos.
  (`public class CantidadLadrillos`).
- Despues se importa la libreria de scanner para ingresar unos datos del usuario.(`import java.util.Scanner;`)
- En el metodo main (`public static void main(String[] args)`)se crea un objeto de escanner llamado input el cual le va a ingresar datos las variables que se van a crear.(`Scanner input = new Scanner(System.in);`)
- Se crean unas varibles para almacenar los datos ingresdos por el usuario con le tipo de dato double
  (`double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;`).
- Se imprimen unos mensajes por pantalla para indicarle al usuario que debe de ingresarle a la varible (`System.out.print("Ingrese el largo de la pared en metros: ");
    largo = input.nextDouble();
    System.out.print("Ingrese el alto de la pared en metros: ");
    alto = input.nextDouble();
    System.out.print("Ingrese el ancho de la pared en metros: ");
    ancho = input.nextDouble();`)

   los datos que ingrese se almacenaran en la variables de alto, largo , ancho de la pared.

   - Despues le pide al usurio imprimiendo mensajes por pantalla las dimensiones del ladrillo
   
   (`System.out.print("Ingrese el largo del ladrillo en metros: ");
      largoLadrillo = input.nextDouble();
      System.out.print("Ingrese el alto del ladrillo en metros: ");
      altoLadrillo = input.nextDouble();
      System.out.print("Ingrese el ancho del ladrillo en metros: ");
      anchoLadrillo = input.nextDouble();`)

 Estas dimensiones se almacenan en las variables de largo, alto y ancho de ladrillo.
    
- Depues se crea una varaible que va a  hacer una operacion para hayar el area de la pared(` double areaPared = largo * alto;`) en este caso multiplica el ancho por alto de la pared.
- Despues de esto se calcula en otra varible el area de ladrillo(`double areaLadrillo = largoLadrillo * altoLadrillo;`)

- Despues se crea la varible la cual va a alamecnar el resulatado de la opercion para mostrar la cantidad de ladrillos que necesita el math ceil lo que hace es redonder un numero decimal a un numero entero hacia arriba
 (`cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));`)
 - Por ultimo se imprime un mensaje con la cantdidad de ladrillos que necesita para contruir la pared(`System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);`).

 ## Calcular el movimiento rectilíneo uniforme
El movimiento rectilíneo uniforme (MRU) es un tipo de movimiento en el cual un objeto se mueve en línea recta y a velocidad constante, es decir, su velocidad no cambia en el tiempo. En este tipo de movimiento, la trayectoria del objeto es una línea recta, por lo que su aceleración es cero.

Un ejemplo común de MRU es un automóvil que se desplaza en una carretera recta y mantiene una velocidad constante durante todo el trayecto. Otro ejemplo es una pelota que cae verticalmente al suelo sin ser afectada por la resistencia del aire.

El MRU es un movimiento importante en la física, ya que permite entender conceptos básicos como la velocidad, la distancia recorrida y el tiempo de desplazamiento. Además, es utilizado como base para otros tipos de movimiento más complejos, como el movimiento rectilíneo uniformemente acelerado (MRUA) y el movimiento circular uniforme (MCU).

Ejemplo en Java de cómo calcular el movimiento rectilíneo uniforme:
```java 

import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}
```

En este programa, primero se solicita al usuario que ingrese la velocidad en metros por segundo y el tiempo en segundos.

A continuación, se calcula la distancia recorrida utilizando la fórmula distancia = velocidad x tiempo, donde la velocidad se mide en metros por segundo, el tiempo se mide en segundos y la distancia se mide en metros.

Finalmente, se muestra el resultado en la consola utilizando el método printf de la clase System.out.

# Explicacion del ejercicio Movimiento rectilíneo uniforme

Para realizar realizar este ejersicio se se llevan acabo los sigientes puntos:

1. la creacion de un proyecto llama MRU lo cual indica movimiento rectilineo uniforme.(`public class MRU ,
   public static void main(String[] args) `)
2. Crear un objeto de la clase Scanner llamado input
 el cual tomara los datos ingresados por el usuario(` Scanner input = new Scanner(System.in);`)
3. Se importa la libreria de Scanner(`
import java.util.Scanner;`)
4. se crean la variables velocidad, tiempo, distancia con el tipo de dato double.(`double velocidad, tiempo, distancia;`)
5. se imprime un menseje al usuario indicando que ingresar en la variables de velocidad y tiempo.(`  System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();`)
6. en la variable distancia a tomar el resulatado de los datos ingresados por el usuario donde va a multiplicar la velocidad por el timpo recorrido.(` distancia = velocidad * tiempo;`)
7. se impreme el resultado en pantalla de la distancia recorrida en movimineto rectilineo uniforme(` System.out.printf("La distancia recorrida es de %.2f metros.", distancia);`).







