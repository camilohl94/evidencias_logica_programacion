<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 6

<!-- Su documentación aquí -->

# Documentacion del proyecto integrdor calculos mecanicos.

- En este programa tenemos varias opciones que el clinete puede consultar las cuales son preguntas que  relacionamos con el diario vivir de los propietarios de vehiculos. Entre las opciones esta  calcular velocidad promedio a la cual viajaron en su vehiculo con una distancia y un tiempo determinado ,en la opcion de  calcular autonomia  de  un vehiculo  es básicamente la distancia máxima que puede llegar a circular un vehículo sin necesidad de parar a repostar, es decir, hasta que tengamos que rellenar el combustible otra vez. y en la opcion  consumo de su motor por distacncia recorrida es muy util para llevar un control de consumo de su maquina  y  estar atento llegado el caso de que el consumo aumente.

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

# Diagrama de flujo:

![Imagen de diagrama de flujo](https://firebasestorage.googleapis.com/v0/b/proyecto-integrador-5260a.appspot.com/o/diagrama%20de%20flujo%20proyecto%20integrador1.png?alt=media&token=09d3cbdb-0c0b-41fd-bbc0-59efbdb591cc&_gl=1*1bkrphe*_ga*MTMwNzIxNTExNS4xNjk0OTE0Mjc3*_ga_CW55HF8NVT*MTY5Njc4MDMwMC4xNC4xLjE2OTY3ODA3NzEuNTYuMC4w)

# Documentacion del proyecto integrador simulador caida libre de una pelota.
Este ejercicio tiene como objetivo simular la caída libre de una pelota desde una altura inicial determinada bajo la influencia de la gravedad. La idea es calcular y mostrar varios aspectos del movimiento de la pelota, incluyendo el tiempo que tarda en caer y la velocidad con la que impacta en el suelo.

```java
import java.util.Scanner;

public class ProyectoIntegrador_2 {

    public static void main(String[] args) {
        
     Scanner entradaDatos = new Scanner(System.in);   

        // Aceleración debido a la gravedad (m/s²)
        double gravedad = 9.81;

        // Solicitar al usuario la altura inicial desde la que caerá el objeto (metros)
        System.out.print("Ingrese la altura inicial desde la que caerá el objeto (metros): ");
        double alturaInicial =entradaDatos.nextDouble();

        // Calcular el tiempo que tarda en caer el objeto hasta el suelo
        //math.sqrt es por que se debe sacar la raiz cudrada de esa operacion.
        
        double tiempo = Math.sqrt((2 * alturaInicial) / gravedad);

        // Calcular la velocidad final al impactar con el suelo
        
        double velocidadFinal = gravedad * tiempo;

        // Mostrar los resultados
        System.out.println("El objeto tarda " + tiempo + " segundos en caer.");
        System.out.println("La velocidad final al impactar con el suelo es " + velocidadFinal + " m/s.");

        // Simular el movimiento en intervalos de tiempo
        double tiempoActual = 0.0;
        double intervaloTiempo = 0.1; // Intervalo de tiempo en segundos
        
        
        System.out.println("Simulación del movimiento:");
        System.out.println("Tiempo (segundos)   Altura (metros)");
        
        while (tiempoActual <= tiempo) {
            double altura = alturaInicial - (0.5 * gravedad * Math.pow(tiempoActual, 2));
            System.out.println(tiempoActual + "segundos           " + altura + "metros");
            tiempoActual += intervaloTiempo;
        }
    }
}
```
## Diagrama de flujo:
![imagen e daigram de flujo](https://firebasestorage.googleapis.com/v0/b/proyecto-integrador-5260a.appspot.com/o/diagrama%20de%20flujo%20proyecto%20integrador%202.png?alt=media&token=9106ccdd-d72c-4302-8a8d-9584a6235e7a&_gl=1*83018j*_ga*MTMwNzIxNTExNS4xNjk0OTE0Mjc3*_ga_CW55HF8NVT*MTY5Njc4NzE3MS4xNS4xLjE2OTY3ODcyMDIuMjkuMC4w)


