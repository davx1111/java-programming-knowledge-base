# Fundamentos de Java — Base Teórica y Conceptual

> Documento de estudio personal que resume los fundamentos esenciales del ecosistema Java,
> su arquitectura de ejecución y las bases del lenguaje desde una perspectiva práctica.

---

## ¿Qué es Java?

Java es un lenguaje de programación orientado a objetos que se ejecuta sobre una máquina virtual (JVM),
lo que permite que el código compilado pueda correr en múltiples sistemas operativos.

### Ediciones principales

- **Java SE (Standard Edition)**
  - Núcleo del lenguaje
  - Aplicaciones standalone y desktop
  - Base para aprender Java

- **Java EE (Enterprise Edition)**
  - Aplicaciones empresariales
  - Procesamiento del lado del servidor

---

## Componentes del Ecosistema Java

### JVM — Java Virtual Machine
- Ejecuta el bytecode compilado
- Permite portabilidad multiplataforma

### JRE — Java Runtime Environment
- Librerías necesarias para ejecutar programas Java

### JDK — Java Development Kit
- Herramientas para desarrollo
- Incluye compilador `javac`

---

## ¿Cómo funciona la ejecución de Java?

### Flujo de compilación

Archivo.java → javac → Archivo.class (Bytecode)


### Flujo de ejecución



Class Loader → Bytecode Verifier → Java Runtime → Sistema Operativo


El bytecode NO se ejecuta directamente en el sistema operativo.

---

## API de Java

La API contiene:

- Clases
- Métodos
- Constructores
- Documentación oficial

Ejemplo de navegación:

1. Módulo → `java.base`
2. Paquete → `java.util`
3. Clase → `Scanner`

Documentación oficial:
https://docs.oracle.com/en/java/javase/17/docs/api/

---

## Principio Fundamental

> Todo en Java es una clase.

---

## Punto de Entrada de un Programa

```java
public static void main(String[] args)


Método principal

Inicio de ejecución

Recibe argumentos de consola

Ejemplo — Hola Mundo
public class HolaMundo {

    public static void main(String[] args) {
        System.out.println("Hola Mundo");
    }
}

Tipos de Datos Primitivos
Enteros

byte

short

int

long

Decimales

float

double

Otros

boolean → true / false

char → 'a'

Primitivos vs Clases
Característica	Primitivos	Clases
Métodos	❌	✅
Herencia	❌	✅
Propiedades	❌	✅
Almacenamiento directo	✅	❌
🔒 Constantes
final int EDAD = 27;

Conversión de Tipos

Ejemplo:

float numero = (float) 10.5;

Operadores

Aritméticos

Relacionales

Lógicos

Asignación

Unarios

Estructuras de Control
IF / ELSE
if(condicion){
}

SWITCH

Casos múltiples según expresión.

Ciclos
FOR
for(int i = 0; i < 10; i++){
}

WHILE

Evalúa antes de ejecutar.

DO WHILE

Ejecuta al menos una vez.

Ciclos Anidados

Principio:

Ciclo externo → estructura

Ciclo interno → contenido

Ejemplo:

for (int col = 1; col <= 3; col++) {
    for (int cont = 1; cont <= 3; cont++) {
        System.out.println(col + " " + cont);
    }
}

Ejercicios Propuestos

Calculadora de comisiones

Días del mes con switch

Impresión de patrones con ciclos

Reflexión Técnica Personal

Durante el estudio de Java se vuelve evidente la importancia de:

Comprender el flujo de ejecución (compilación vs runtime)

Dominar tipos de datos antes de estructuras complejas

Entender profundamente los ciclos para resolver problemas reales

