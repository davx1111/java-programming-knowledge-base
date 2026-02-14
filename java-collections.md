#  Java Collections Framework — ArrayList, HashSet, HashMap e Iterator

> Documento de estudio personal que resume las estructuras principales del Java Collections Framework,
> su comportamiento, características y aplicaciones prácticas en el desarrollo de software.

---

## Introducción a las Colecciones en Java

Las colecciones en Java son estructuras dinámicas que permiten almacenar y manipular grupos de objetos de manera eficiente.

**Permiten:**
- Almacenamiento dinámico
- Organización estructurada de datos
- Eliminación de duplicados
- Asociación clave-valor
- Recorridos controlados

### Importante

Las colecciones **NO** almacenan tipos primitivos directamente.
Se deben usar clases **Wrapper**:

| Tipo primitivo | Clase Wrapper |
|----------------|---------------|
| `int`          | `Integer`     |
| `double`       | `Double`      |
| `char`         | `Character`   |

**Ejemplo:**
```java
ArrayList<Integer> numeros = new ArrayList<>();
```

---

##  List — ArrayList

###  Concepto

`ArrayList` es una implementación de la interfaz `List` que funciona como un arreglo dinámico.

### Características

- Mantiene orden por índice
- Permite elementos duplicados
- Tamaño dinámico
- Inserción automática al final
- Acceso rápido por índice

###  Sintaxis
```java
ArrayList<String> lista = new ArrayList<>();
```

### Métodos principales

| Método            | Función                  |
|-------------------|--------------------------|
| `add(E e)`        | Agrega elemento          |
| `add(int i, E e)` | Inserta en índice        |
| `get(int i)`      | Obtiene elemento         |
| `set(int i, E e)` | Reemplaza                |
| `remove(int i)`   | Elimina                  |
| `size()`          | Tamaño                   |
| `isEmpty()`       | Verifica vacío           |
| `contains()`      | Busca elemento           |
| `clear()`         | Limpia lista             |
| `subList(a, b)`   | Sublista                 |

###  Ejemplo práctico
```java
ArrayList<Integer> numeros = new ArrayList<>();
numeros.add(10);
numeros.add(20);
System.out.println(numeros.get(0)); // Output: 10
```

---

##  Set — HashSet

### Concepto

`HashSet` implementa la interfaz `Set` y representa un conjunto de elementos únicos.

### Características

- No mantiene orden
- No permite duplicados
- Utiliza `hashCode` internamente
- Búsqueda rápida

###  Sintaxis
```java
HashSet<String> autos = new HashSet<>();
```

### 🔧 Métodos principales

| Método       | Función              |
|--------------|----------------------|
| `add()`      | Inserta elemento     |
| `contains()` | Verifica existencia  |
| `remove()`   | Elimina              |
| `size()`     | Cantidad             |

###  Ejemplo
```java
HashSet<String> autos = new HashSet<>();
autos.add("Toyota");
autos.add("Mazda");
autos.add("Toyota"); // No se duplicará
```

---

##  Map — HashMap

###  Concepto

`HashMap` es una estructura basada en pares clave-valor.

- Cada llave es única
- Una llave corresponde a un solo valor
- Utiliza el método `put()` para insertar elementos

###  Sintaxis
```java
HashMap<String, Integer> edades = new HashMap<>();
```

### 🔧 Métodos principales

| Método          | Función            |
|-----------------|-------------------|
| `put(K, V)`     | Inserta elemento  |
| `get(K)`        | Obtiene valor     |
| `containsKey()` | Verifica llave    |
| `remove()`      | Elimina           |
| `keySet()`      | Obtiene llaves    |
| `values()`      | Obtiene valores   |

### Ejemplo
```java
HashMap<String, Integer> edades = new HashMap<>();
edades.put("David", 27);
edades.put("Maya", 26);
System.out.println(edades.get("David")); // Output: 27
```

---

## Iterator

### Concepto

`Iterator` es un objeto que permite recorrer colecciones elemento por elemento sin utilizar índices.

### Ventajas

- Recorrido seguro
- Acceso secuencial
- No depende de posiciones
- Ideal para recorridos externos

### Sintaxis
```java
Iterator<Integer> iterator = numeros.iterator();
```

### Ejemplo
```java
Iterator<Integer> iterator = numeros.iterator();
int total = 0;
while(iterator.hasNext()) {
    total += iterator.next();
}
System.out.println(total);
```

---

## Comparación General

| Estructura  | Orden | Duplicados      | Índices | Uso principal             |
|-------------|-------|-----------------|---------|---------------------------|
| `ArrayList` | Sí    | Sí              | Sí      | Listas dinámicas          |
| `HashSet`   | No    | No              | No      | Conjuntos únicos          |
| `HashMap`   | No    | Llaves únicas   | No      | Asociaciones clave-valor  |

---

## Aplicaciones Prácticas

- **ArrayList** → Listas de usuarios, registros dinámicos
- **HashSet** → Eliminación de duplicados
- **HashMap** → Diccionarios y configuraciones
- **Iterator** → Recorridos controlados

---

## Licencia

Este documento es de uso personal y educativo.

## Autor

Documento de estudio personal sobre Java Collections Framework.




