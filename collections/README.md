#### ESTRUCTURA 6
# Collections, json y manejo de datos

---

1. **Describa el por qué y para qué se utiliza.**
   **¿Por qué?**
      - Collections: Porque facilitan la manipulación y almacenamiento de grandes volúmenes de datos en memoria de manera eficiente.
      - Json: Porque es clave para la comunicación entre aplicaciones y el almacenamiento estructurado.
      - Manejo de datos: Porque permite leer, escribir y procesar información de archivos o bases de datos de manera sencilla
   **¿Para qué?**
   - Collections: Para manejar listas de datos en memoria.
   - Json: Para intercambiar datos entre sistemas o guardarlos de forma estructurada.
   - Manejo de datos: Para leer y escribir información en archivos o bases de datos.
--- 
   
2. **Genere un ejemplo internamente en el recuadro.**  

   - Utilice un editor de código para lograrlo.  
```kotlin
fun main() {
    // List: puede tener elementos repetidos y mantiene el orden
    val lista: List<String> = listOf("A", "B", "A")
    println("📋 List:")
    println(lista) // Imprime: [A, B, A]

    // Set: NO permite duplicados y el orden no siempre es garantizado
    val conjunto: Set<String> = setOf("A", "B", "A")
    println("\n✅ Set:")
    println(conjunto) // Imprime: [A, B] (solo una "A")

    // Map: relaciona claves con valores
    val mapa: Map<String, Int> = mapOf("A" to 1, "B" to 2)
    println("\n🗺️ Map:")
    println(mapa) // Imprime: {A=1, B=2}
}

```

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](#)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/maga1407/kotlin/blob/main/collections/imgCollections/codeCollections.png)**

---

### Escribe una nota del cómo funciona la estructura

```kotlin
fun main() {
    // Creamos una lista de estudiantes, con un duplicado ("Laura" aparece dos veces)
    val estudiantes: List<String> = listOf("Laura", "Carlos", "Laura", "Miguel")

    // Convertimos la lista a un Set para eliminar duplicados automáticamente
    // Un Set solo guarda valores únicos
    val estudiantesUnicos: Set<String> = estudiantes.toSet()

    // Creamos un mapa (Map) que asocia cada nombre de estudiante con una calificación (entero)
    val calificaciones: Map<String, Int> = mapOf(
        "Laura" to 90,
        "Carlos" to 75,
        "Miguel" to 88
        // Nota: No hay nota para "Pedro", por ejemplo
    )

    // Mostramos la lista de estudiantes únicos (sin duplicados)
    println("📋 Lista de estudiantes únicos:")
    for (nombre in estudiantesUnicos) {
        println("- $nombre")
    }

    println("\n🎓 Calificaciones:")

    // Recorremos el set de nombres únicos para mostrar las calificaciones
    for (nombre in estudiantesUnicos) {
        // Obtenemos la calificación desde el Map
        // Usamos Int? porque puede que no exista una nota (podría ser null)
        val nota: Int? = calificaciones[nombre]

        // Si la nota no es null, la mostramos
        // Si es null, mostramos que no hay nota registrada
        if (nota != null) {
            println("$nombre: $nota")
        } else {
            println("$nombre: sin nota registrada")
        }
    }
}

```

