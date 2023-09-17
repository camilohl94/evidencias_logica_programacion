<!-- No borrar o modificar -->

[Inicio](./index.md)

## Sesión 4

<!-- Su documentación aquí -->

# Actividad 4: Ejercicios de control de flujo con expresiones compuestas

```java copy
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

**Con la información anterior, implementa los siguientes ejercicios:**

- Determinar si el estudiante es mayor de edad y tiene un estado activo.
- Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
- Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
- Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
- Mostrar toda la información del estudiante si está matriculado en el Cesde.
- Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
- Determinar la cantidad de beca que recibe el estudiante según su promedio:

  - 0.0 - 3.4: El estudiante no recibe beca.
  - 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
  - 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
  - 4.5 - 5.0: El estudiante recibe una beca completa.

  ## Solucion:

```java copy
  package com.mycompany.actividad_controlflujo;

public class Actividad_ControlFlujo {

    public static void main(String[] args) {
        String nombre = "Juan Pérez";
        String apellido = "González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        // Variable de tipo int
        int edad = 20;
        // Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
        // Variable de tipo char
        char genero = 'M';
        // Variable de tipo double
        double promedio = 4.5;
        // Variable de tipo int
        int semestre = 2;

        System.out.println("-----------------------------------------------------------------------------------");
        System.out.println("Ejersicio 1: Determinar si el estudiante es mayor de edad y tiene un estado activo.");
        System.out.println("-----------------------------------------------------------------------------------");
        if (edad >= 18) {
            System.out.println("El estudiante es mayor de edad");
            if (esActivo) {
                System.out.println("el estudiante esta activo");

            } else {
                System.out.println("el estudiante no es ta activo");
            }
        } else {
            System.out.println("El estudiante es menor de edad");
        }

        System.out.println("---------------------------------------------------------------------------------------------------------------");
        System.out.println("ejersicio 2:Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.");
        System.out.println("---------------------------------------------------------------------------------------------------------------");
        if (carrera.equals("Desarrollo de Software") || becado) {
            System.out.println("El estudiante cumple con una o con las dos condicciones");

        }
        System.out.println("---------------------------------------------------------------------------------------------------------");
        System.out.println("ejersicio 3: Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.");
        System.out.println("----------------------------------------------------------------------------------------------------------");

        if (semestre == 3) {
            System.out.println("El estudiante cumple con las condicciones");
        } else if (esActivo) {
            System.out.println("El estudinte no cumple con las condicciones de ultimo semestre pero si esta activo ");
        } else {
            System.out.println("El estudiante no esta en el ultimo semestre ni activo");
        }

        System.out.println("------------------------------------------------------------------------------------------------------------------");
        System.out.println("Ejersicio4: Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.");
        System.out.println("-----------------------------------------------------------------------------------------------------------------------");

        if (carrera.equals("Desarrollo de Software") && promedio >= 4.0) {
            System.out.println("el estudiante cumple con los requisitos");
        }

        System.out.println("-------------------------------------------------------------------------------------------------------");
        System.out.println("Ejersicio5: Mostrar toda la información del estudiante si está matriculado en el Cesde.");
        System.out.println("-------------------------------------------------------------------------------------------------------");

        if (universidad.equals("Cesde")) {
            System.out.println("Nombre del estudiante: " + nombre + "\nApellido del  estudiante: " + apellido
                    + "\nNumero de identrificacion: " + identificación + "\nCorreo: " + correo + "\nNombre de carrera: " + carrera
                    + "\nUniversidad: " + universidad + "\nEdad: " + edad + "\nEstado del estudiante: " + esActivo + "\nTiene alguna beca: " + becado
                    + "\nGenero: " + genero + "\nPromedio del estudiante: " + promedio + "\nSemestre: " + semestre);
        } else {
            System.out.println("El estudiante no esta matriculado en el cesde");
        }
        System.out.println("---------------------------------------------------------------------------------------------------------");
        System.out.println("Ejersicio6: Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.");
        System.out.println("--------------------------------------------------------------------------------------------------------------");

        if (universidad.equals("Cesde") && promedio >= 4.0 && esActivo) {
            System.out.println("El estudiante se a ganado una beca del 50% por cumplir con los requisitos ");

        } else {
            System.out.println("El estudiante no cumple con los requisitos para la beca");
        }
        System.out.println("------------------------------------------------------------------------------------");
        System.out.println(" Ejersicio7: Determinar la cantidad de beca que recibe el estudiante según su promedio:\n"
                + "0.0 - 3.4: El estudiante no recibe beca.\n"
                + "3.5 - 3.9: El estudiante recibe una beca parcial del 25%.\n"
                + "4.0 - 4.4: El estudiante recibe una beca parcial del 50%.\n"
                + "4.5 - 5.0: El estudiante recibe una beca completa.");
        System.out.println("--------------------------------------------------------------------------------------");

        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca. ");

        } else if (promedio >= 3.4 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%. ");

        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%.");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa.");

        }
        System.out.println("-----------------------------------------------------------------------------------------");
        System.out.println("Ejersicio8: Determinar si el estuduiante es hombre puede entrar el equipo de futboll");
        System.out.println("------------------------------------------------------------------------------------------");

        if (genero == 'M') {
            System.out.println("El estudiante puede entrar al equipo de futbol");
        } else {
            System.out.println("El estudiante no puede entrar al equipo de futboll");
        }

        System.out.println("--------------------------------------------------------------------------------------------------------------------");
        System.out.println("Ejersicio9: Determinar si el estudiante tiene una edad mayor o igual a 18 para poder  ingresar al concurso de baile");
        System.out.println("-------------------------------------------------------------------------------------------------------------------");

        if (edad >= 18) {
            System.out.println("El estudiante puede ingresar al concurso de baile");

        } else {
            System.out.println("El estudiante no puede ingresar al concurso de baile");
        }

        System.out.println("--------------------------------------------------------------------------------------------------");
        System.out.println("Ejersicio10: Determinar si el estudiante esta en el segundo semestre para habilitar la plataforma de ingles ");
        System.out.println("---------------------------------------------------------------------------------------------------------------");

        if (semestre == 2) {
            System.out.println("Tienes activa la plataforma de ingles");

        } else {
            System.out.println("La plataforma de ingles esta inactiva");
        }
    }
}
```
