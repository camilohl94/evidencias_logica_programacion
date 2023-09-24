<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->
# Actividad: Ejecicios de métodos en Java

Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.


## Solucion:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

 ```java
 package com.mycompany.actividadsesion8_1;

import java.util.Scanner;

public class ActividadSesion8_1 {

    public static void main(String[] args) {
        encontrarMayor();

    }

    public static void encontrarMayor() {

        Scanner entrada = new Scanner(System.in);
        System.out.println("ingrese el premer numero");
        int n1 = entrada.nextInt();
        System.out.println("ingrese el segundo nuemro");
        int n2 = entrada.nextInt();

        if (n1 > n2) {
            System.out.println("el mayor es:" + n1);

        } else if (n2 > n1) {
            System.out.println("el mayor es" + n2);
        } else if (n1 == n2) {
            System.out.println("numeros iguales");
        }
    }
}
```
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

```java 
package com.mycompany.actividadsesion8_2;

public class ActividadSesion8_2 {

    public static void main(String[] args) {

        int resultado = encontrarVocales("hola mundo");
        System.out.println("numero de vocales son:" + resultado);

    }

    public static int encontrarVocales(String texto) {
        int contador = 0;
        texto = texto.toLowerCase();
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;

            }
        }
        return contador;
        
    }

}
```
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

```java 
package com.mycompany.actividadsesion8_3;

import java.util.Scanner;

public class ActividadSesion8_3 {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);
        System.out.println("ingresa una cadena par convertir ");
        String texto = entrada.nextLine();
        convertirpalabras(texto);

    }

    public static void convertirpalabras(String texto) {
        StringBuilder resultado = new StringBuilder();

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter);
                resultado.toString();

            }

        }
        System.out.println(resultado);
    }
}
```
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

```java
package com.mycompany.actividadsesion8_4;

import java.util.Scanner;

public class ActividadSesion8_4 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner (System.in);
        System.out.println("ingrese su cadena¨:");           
        String cadena = entrada.nextLine();
        contarPalabras(cadena);
        
    }
    public static void contarPalabras(String cadena){
        String [] palabras = cadena.split("\\s+");
        
       int resultado = palabras.length;
        System.out.println("Cantdiad de palabaras escritas:\s"+resultado);
    }
}
```
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

```java 
package com.mycompany.actividadsesion8_5;

import java.util.Arrays;
import java.util.Scanner;

public class ActividadSesion8_5 {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        System.out.println("ingrese una cadena para odenar:");
        String texto = entrada.nextLine();
        ordenarPalabras(texto);
        String textoOrdenado = ordenarPalabras(texto);
        System.out.println(textoOrdenado);

    }

    public static String ordenarPalabras(String texto) {
        String[] palabras = texto.split(" ");
        Arrays.sort(palabras);
        String textoOrdenado = String.join(" ", palabras);
        return textoOrdenado;

    }
}
```












