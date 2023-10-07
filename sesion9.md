<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->

# Actividad: Ejecicios de métodos en Java
Resolver en parejas el ejercicio asignado por el docente.
## Calculadora de resistencias eléctricas
Una resistencia eléctrica es un componente electrónico que se utiliza para limitar el flujo de corriente eléctrica en un circuito. Es decir, su función es oponerse al paso de la corriente eléctrica y disminuir su intensidad.

Las resistencias se componen generalmente de un material conductor, como el carbono o el metal, que se coloca en un cuerpo cerámico o de vidrio. El valor de la resistencia (es decir, la cantidad de oposición que ofrece al paso de la corriente eléctrica) se mide en ohms, y depende de la composición del material y de su geometría.

Las resistencias se utilizan en una gran variedad de circuitos electrónicos, tanto en circuitos analógicos como digitales. Algunas de las aplicaciones más comunes de las resistencias incluyen la limitación de corriente en circuitos de alimentación, el ajuste de niveles de voltaje y corriente en circuitos de amplificación, y la medición de corriente y voltaje en circuitos de control y monitoreo.

![Imagen de resistencia](https://f47ec6e8ca.cbaul-cdnwnd.com/b9a0fcea3766057deaebf52a7956b29e/200000057-e1c97e3bbe/codigo%20de%20colores.png)

El objetivo de este ejercicio es crear un programa en Java que permita calcular el valor de una resistencia eléctrica a partir de los colores de sus bandas, y que tenga en cuenta la tolerancia.

Para ello, el programa debe solicitar al usuario que elija los colores de las tres bandas de la resistencia a través de un menú de opciones. Los colores disponibles son: negro, marrón, rojo, naranja, amarillo, verde, azul, violeta, gris y blanco.

Una vez que el usuario ha elegido los colores de las tres bandas, el programa debe pedir al usuario que seleccione la tolerancia de la resistencia a través de otro menú de opciones. Las opciones disponibles son: marrón (1%), rojo (2%), oro (5%) y plata (10%). Si el usuario no selecciona ninguna opción válida, se debe utilizar la tolerancia por defecto del 5%.

Con los colores y la tolerancia seleccionados, el programa debe calcular el valor de la resistencia y mostrarlo en la consola, junto con la tolerancia seleccionada.

Para calcular el valor de la resistencia, se debe utilizar la fórmula: valor = ((valor1 10) + valor2) multiplicador, donde valor1 y valor2 son los valores correspondientes a los dos primeros colores elegidos por el usuario (según la tabla de colores), y multiplicador es el valor correspondiente al tercer color elegido por el usuario (también según la tabla de colores). Finalmente, se debe mostrar el valor de la resistencia en ohms y la tolerancia seleccionada.


# Solucion:
``` java
package com.mycompany.calculadoraresistencia;

import java.util.Scanner;

public class CalculadoraResistencia {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        calcularResistencia("banda1");
        System.out.println("ingrese el primer color: ");
        int banda1 = sc.nextInt();
        calcularResistencia("banda2");
        System.out.println("ingrese el segundo color: ");
        int banda2 = sc.nextInt();
        calcularResistencia("banda3");
        System.out.println("ingrese el Tercer color: ");
        int banda3 = sc.nextInt();

        int operacion1 = (banda1 * 10) + banda2;

        switch (banda3) {
            case 0 ->
                operacion1 *= 1;
            case 1 ->
                operacion1 *= 10;
            case 2 ->
                operacion1 *= 100;
            case 3 ->
                operacion1 *= 1000;
            case 4 ->
                operacion1 *= 10000;
            case 5 ->
                operacion1 *= 100000;
            case 6 ->
                operacion1 *= 1000000;
            case 7 ->
                operacion1 /= 10;
            case 8 ->
                operacion1 /= 100;
            case 9 -> {
            }

        }
        String resisitenciaFormateda = "";
        if (operacion1 >= 1000) {
            double valork = operacion1 / 1000;
            resisitenciaFormateda = valork + "k";
        } else {
            resisitenciaFormateda = String.valueOf(operacion1);
        }
        System.out.println("Resistencia sin tolerancia:" + resisitenciaFormateda + " ohmios");
        calcularTolerancia();
        int banda4 = sc.nextInt();

        switch (banda4) {
            case 0 ->
                operacion1 *= 1;
            case 1 ->
                operacion1 *= 5;
            case 3 ->
                operacion1 *= 10;

            default ->
                operacion1 *= 5;

        }
        int resistenciaConTolerancia = operacion1 / 100;

        if (resistenciaConTolerancia >= 1000) {
            double valork = resistenciaConTolerancia / 1000;
            resisitenciaFormateda = valork + "k";
        } else {
            resisitenciaFormateda = String.valueOf(resistenciaConTolerancia);
        }

        System.out.println("la tolerancia de esta resistencia es : " + resisitenciaFormateda + " ohmios");
    }

    public static void calcularResistencia(String banda) {
        Scanner sc = new Scanner(System.in);

        System.out.println("""
                           Colores de resistencia:
                           o. negro
                           1. marron
                           2. rojo
                           3. naranja
                           4. amarillo
                           5. verde
                           6. azul
                           7. purpura
                           8. gris
                           9. blanco
                           Elija el numero del color para calcular la resistencia:""");

    }

    public static void calcularTolerancia() {
        System.out.println("""
                           Seleccione el color de la tolerancia:
                           0. marron = 1%
                           1. rojo = 2%
                           2. oro =5%
                           3 plata = 10%
                           Ingrese el color de la tolerancia:""");

    }


```



