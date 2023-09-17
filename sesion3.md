<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 3

<!-- Su documentación aquí -->

# Actividad 3: Ejercicios de operaciones básicas en Java.

## Suma y multiplicación:

Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

### Solucion:

```java copy
import java.util.Scanner;


public class ActividadSesion3_2 {

    public static void main(String[] args) {

        Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer numero:");
        int num1 = entradaDatos.nextInt();

        System.out.println("Ingrese el segundo numero:");
        int num2 = entradaDatos.nextInt();

        int suma = num1 + num2;
        int multiplicacion = num1 * num2;

        System.out.println("El resultado de la suma de los dos numeros es: " + suma);
        System.out.println("El resultado de la multipliccion de los dos numeros es: " + multiplicacion);

    }
}
```

## Resta y división:

Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

### Solucion:

```java copy
 import java.util.Scanner;

public class ActividadSesion3 {

    public static void main(String[] args) {

        Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer numero:");
        int num1 = entradaDatos.nextInt();

        System.out.println("Ingrese el segundo numero:");
        int num2 = entradaDatos.nextInt();

        int Resta = num1 - num2;
        int Division = num1 / num2;

        System.out.println("El resultado de la Resta de los dos numeros es: " + Resta);
        System.out.println("El resultado de la Division de los dos numeros es: " + Division);
    }
}
```

## Operaciones combinadas:

Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

### Solucion:

```java copy
 import java.util.Scanner;


public class ActividadSesion3_3 {

    public static void main(String[] args) {
         Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer numero:");
        int num1 = entradaDatos.nextInt();

        System.out.println("Ingrese el segundo numero:");
        int num2 = entradaDatos.nextInt();

        System.out.println("Ingresa el tercer numero: ");
        int num3 = entradaDatos.nextInt();

        int operacion1 = num1 + num2 + num3;
        int operacion2 = (num1*num2)/num3;

        System.out.println("El resultado de la suma de los tres numeros es : " +operacion1);
        System.out.println("El resultado de la multiplicacion del primer numero por el segundo y division por el tercer numero es: "+operacion2);

    }
}
```

## Operaciones con decimales:

Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

### Solucion:

```java copy
 import java.util.Scanner;


public class ActividadSesion3_4 {

    public static void main(String[] args) {
         Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer numero decimal:");
        float num1 = entradaDatos.nextFloat();

        System.out.println("Ingrese el segundo numero decimal:");
        float num2 = entradaDatos.nextFloat();

        float suma = num1+ num2;
        float resta = num1-num2;
        float multiplicacion = num1*num2;
        float division = num1/ num2;

        System.out.println("El resultado de la suma es: "+suma);
        System.out.println("El resultdo de la resta es: "+resta);
        System.out.println("El resultdo de la multuplicacion es: "+multiplicacion);
        System.out.println("El resultdo de la division es: "+division);
    }
}
```

## Incremento y decremento:

Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

### Solucion:

```java copy
 public class ActividadSesion3_5 {

    public static void main(String[] args) {

        int numero = 24;

        numero += 1;

        System.out.println("el resultado de incremento del numero es: " + numero);
        numero -= 1;
        System.out.println("el resultado del decremento del numero es: " + numero);

    }
}
```

## Operador de asignación compuesta:

Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

### Solucion:

```java copy
 public class ActividadSesion3_6 {

    public static void main(String[] args) {
        int numero = 34;
        numero += 5;
        System.out.println("El resultado de la asignacion compueta mas 5 es:" + numero);
    }
}
```

## Operadores lógicos:

Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

### Solucion:

```java copy
import java.util.Scanner;


public class ActvidadSesion3_7 {

    public static void main(String[] args) {
        Scanner entradaDatos = new Scanner(System.in);

        System.out.println("ingresos para el trampolin");

        System.out.println("su peso es menor que 40:");
        boolean peso = entradaDatos.hasNextBoolean();

        System.out.println("su edad es menor que 10");
        boolean edad = entradaDatos.hasNextBoolean();

        boolean ingresoTrampolin1 = edad && peso;
        boolean ingresoTrampolin2 = !edad;
        boolean ingresoTrampolin3 = !peso;
        boolean ingreseTrampolin4 = edad || peso;

        System.out.println("Resultado de ingreso al trampolin1 es: " + ingresoTrampolin1);
        System.out.println("Resultado de ingreso al trampolin2 es: " + ingresoTrampolin2);
        System.out.println("Resultado de ingreso al trampolin3 es: " + ingresoTrampolin3);
        System.out.println("Resultado de ingreso al trampolin2 es:" + ingreseTrampolin4);

    }
}
```

## Operador ternario:

Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

### Solucion:

```java copy
import java.util.Scanner;


public class ActividadSesion3_8 {

    public static void main(String[] args) {

        Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Por favor ingresa un numero: ");
        int numero = entradaDatos.nextInt();

        if (numero == 0) {
            System.out.println("el numero es neutro");
        }
        else if (numero<=0){System.out.println("el numero es negativo");
        }else { System.out.println("el numero es positivo");}

    }
}
```
