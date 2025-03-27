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

🔗 **[LINK DE CODIGO](#)** 

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](#)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/maga1407/kotlin/blob/main/collections/collectios.png)**

---

### Escribe una nota del cómo funciona la estructura

```kotlin
// Importamos las funciones necesarias para manejar JSON en Kotlin
import kotlinx.serialization.json.*

fun main() {
    // LISTAS (List)
    // Una lista (List) es una colección ordenada de elementos.
    // En este caso, la lista contiene varios mapas (Map).
    val estudiantes = listOf(
        // MAPAS (Map)
        // Un mapa (Map) es una estructura de datos que almacena pares clave-valor.
        // En este caso, cada mapa representa un estudiante con su nombre y nota.
        mapOf("nombre" to "Ana", "nota" to 4.5),
        mapOf("nombre" to "Luis", "nota" to 3.8),
        mapOf("nombre" to "Carlos", "nota" to 4.2)
    )

    // CONVERTIR LA LISTA A JSON
    // JSON (JavaScript Object Notation) es un formato de texto usado para almacenar y transportar datos.
    // La función encodeToString convierte la lista a una cadena JSON.
    val jsonString = Json.encodeToString(estudiantes)
    println("JSON generado:\n$jsonString")

    // CONVERTIR EL JSON A UNA LISTA DE MAPAS
    // La función decodeFromString transforma el JSON en una estructura de datos nuevamente.
    val listaRecuperada: List<Map<String, Any>> = Json.decodeFromString(jsonString)

    // MOSTRAR LOS DATOS RECUPERADOS
    // Iteramos sobre la lista recuperada para imprimir cada estudiante y su nota.
    println(" Lista de estudiantes recuperada desde JSON:")
    listaRecuperada.forEach { estudiante ->
        println("${estudiante["nombre"]}, Nota: ${estudiante["nota"]}")
    }
}

```

