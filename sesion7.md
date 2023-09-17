<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 7

<!-- Su documentación aquí -->

# Actividad: Ejecicios Array - ArrayList

1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

**Ejemplo Array:**

```java
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```

```java
Ejemplo Array list
import java.util.ArrayList;
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();

    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {

    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();

    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();

    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
```

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

## Solucion:

**Ejemplo de array:**

```java
public class ArraySesion7 {

    public static void main(String[] args) {
        System.out.println("------------------------------------------------------------------------------");
        System.out.println("ejersicio integrando array");
        System.out.println("-------------------------------------------------------------------------------");

        System.out.println("Mostrar la cantidad de empresas ingresadas en el array:");
        System.out.println("------------------------------------------------------------------------------");

        String[] empresas = {"epm", "tigo", "yamaha", "toyota", "sura", "coordinadora", "akt", "americanino"};
        // este mando nos imprime el numero de empresas ingresadas
        System.out.println("cantidad de empresas: " + empresas.length);
        System.out.println("------------------------------------------------------------------------------");
        System.out.println("mostrar la lista de empresas empresas: ");
        System.out.println("-------------------------------------------------------------------------------");
        System.out.println("las empresas ingresadas en el arreglo son:");

        for (int i = 0; i < empresas.length; i++) {
            System.out.println(empresas[i]);

        }
        System.out.println("-------------------------------------------------------------------------------");
        System.out.println("sacar una empresa del listado:");
        System.out.println("-------------------------------------------------------------------------------");
        for (String i : empresas) {

            if (empresas[7] == i) {
                continue;
            }
            System.out.println(i);
        }

        System.out.println("---------------------------------------------------------------------------------");
        System.out.println("imprimir la ultima empresa ingresada: ");

        System.out.println(empresas[7]);

    }

}
```

**Ejemplo de arrayList:**

```java
public class ArrayListSesion7 {

    public static void main(String[] args) {
        Scanner entradaDatos = new Scanner(System.in);
        ArrayList<String> empresas = new ArrayList<>();
        empresas.add("exito");
        empresas.add("\nd1");
        empresas.add("\nsurtimax");
        empresas.add("\njumbo");
        empresas.add("\ncarulla");
        empresas.add("\nla rebaja");
        empresas.add("\nbonansa");

        System.out.println(" lista de empresas:");
        for (String empresa : empresas) {
            System.out.println(empresa);
        }
        System.out.println("cantidad de empresas:");
        int size = empresas.size();
        System.out.println(size);
        System.out.println("se elimina una empresa de la lista");
        System.out.println("nueva lista:");
        empresas.remove(2);
        for (String empresa : empresas) {
            System.out.println(empresa);
        }

}
}
```
