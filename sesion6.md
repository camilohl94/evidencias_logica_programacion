<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 6

<!-- Su documentación aquí -->

# Documentacion del proyecto integrador

- En este programa tenemos varias opciones para consultar como calcular velocidad, calcular autonomia y consumo de su motor en la cual le hace una operacion y le muestra el reultado de su consulta.

```java
package com.mycompany.casointegrador_1;

import java.util.Scanner;


public class CasoIntegrador_1 {

    @SuppressWarnings("fallthrough")
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        boolean repetir = true;
        while (repetir) {
            System.out.println("""
                               por favor elija una opcion:
                                1. Calcular el consumo de su motor por distancia recorrida
                                2. Calcular velocidad promedio
                                3. Calcular autonomia
                                4. salir """);
            int numero = entrada.nextInt();

            switch (numero) {
                case 1:
                    calcularConsumo();
                    break;
                case 2:
                    calcularVelocidad();
                    break;
                case 3:
                    calcularAutonomia();
                    break;
                case 4:
                    repetir = false;
                default:
                    System.out.println("opcion no valida");
                    break;
            }
        }
    }

    public static void calcularConsumo() {
        Scanner entrada = new Scanner(System.in);
        System.out.println("por favor ingrese el kilometraje recorrido: ");
        double kilometraje = entrada.nextDouble();
        System.out.println("Por favor ingrese la cantidad de combustible gastado en litros: ");
        double consumo = entrada.nextDouble();
        double resultado = kilometraje / consumo;
        System.out.println("el consumo de su motor por kilometraje es : " + resultado + " km/l ");

    }


    public static void calcularVelocidad() {
        Scanner entrada = new Scanner(System.in);
        System.out.println("por favor ingrese el kilometraje recorrido: ");
        double kilometraje = entrada.nextDouble();
        System.out.println("Por favor ingrese el tiempo que se demoro en horas: ");
        double tiempo = entrada.nextDouble();
        double resultado = kilometraje/tiempo;
        System.out.println("Su velocidad promedio es: " + resultado + "km/h");

    }

    public static void calcularAutonomia() {
        Scanner entrada = new Scanner(System.in);
        System.out.println("por favor ingrese la capacidad de su tanque en litros: ");
        double capacidad = entrada.nextDouble();
        System.out.println("ingrese el consumo de combustible en km/l: ");
        double consumo = entrada.nextDouble();
        double resultado = capacidad * consumo;
        System.out.println("la autonomia de su moto es de " + resultado + " kilometros con el tanque actual.");
    }
}

```
