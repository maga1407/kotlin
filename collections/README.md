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

🔗 **[LINK DE CODIGO]()** 

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO]()**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB]()**

---

### Escribe una nota del cómo funciona la estructura

```
import kotlinx.serialization.*
import kotlinx.serialization.json.*
import java.io.File

// Definir la clase de datos y habilitar JSON
@Serializable
data class Estudiante(val nombre: String, val edad: Int)

fun main() {
    // Crear una colección de estudiantes (List)
    val estudiantes = listOf(
        Estudiante("Ana", 20),
        Estudiante("Luis", 22),
        Estudiante("Carlos", 19)
    )

    // Convertir la lista a JSON
    val jsonString = Json.encodeToString(estudiantes)
    println("JSON generado:\n$jsonString")

    // 📌 4. Guardar el JSON en un archivo
    val archivo = File("estudiantes.json")
    archivo.writeText(jsonString)
    println("✅ Datos guardados en estudiantes.json")

    // 📌 5. Leer el JSON desde el archivo
    val contenido = archivo.readText()
    println("📂 JSON leído desde el archivo:\n$contenido")

    // 📌 6. Convertir el JSON nuevamente a una lista de objetos
    val estudiantesLeidos = Json.decodeFromString<List<Estudiante>>(contenido)
    println("📌 Lista de estudiantes recuperada desde JSON:")
    estudiantesLeidos.forEach { println("${it.nombre}, ${it.edad} años") }
}
```

