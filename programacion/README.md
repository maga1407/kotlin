#### ESTRUCTURA 8
# PROGRAMACIÓN FUNCIONAL Y EXEPCIONES LAMBDA 

---

1. **Describa el por qué y para qué se utiliza.**

La **programación funcional** se utiliza para escribir código más claro, predecible y sin efectos secundarios, lo que facilita su mantenimiento y reduce errores. Es ideal para procesar datos mediante funciones como `map`, `filter` y `reduce`, usando un estilo declarativo. Las **expresiones lambda** son funciones anónimas que permiten definir operaciones breves en una sola línea, especialmente útiles como argumentos en funciones. Ambas herramientas permiten trabajar de forma más eficiente y expresiva en lenguajes modernos como Python, Java, Kotlin o JavaScript.

   
2. **Genere un ejemplo internamente en el recuadro.**  

   - Utilice un editor de código para lograrlo.  

🔗 **[LINK DE CODIGO](https://pl.kotl.in/rm87TQL9t)** 

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/user-attachments/assets/9cf8ccaf-8d99-41e4-9308-cd7fe10f9980)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](![ejercicio1](https://github.com/user-attachments/assets/831fb00b-183f-4f40-8749-816a24060e12)
)**

---

### Escribe una nota del cómo funciona la estructura  

data class Estudiante(val nombre: String, val edad: Int, val nota: Double)

fun main() {

    val estudiantes = listOf(
        Estudiante("Ana", 20, 8.5),
        Estudiante("Luis", 22, 5.8),
        Estudiante("María", 21, 9.2),
        Estudiante("Carlos", 19, 4.7),
        Estudiante("Sofía", 23, 7.0)
    )

    // 1. Filtrar estudiantes aprobados (nota >= 6.0)
    val aprobados = estudiantes.filter { it.nota >= 6.0 }

    // 2. Obtener solo los nombres de los aprobados
    val nombresAprobados = aprobados.map { it.nombre }

    // 3. Calcular el promedio de nota de los aprobados
    val promedioAprobados = aprobados.map { it.nota }.average()

    // 4. Agrupar estudiantes por si aprobaron o no
    val agrupados = estudiantes.groupBy { it.nota >= 6.0 }

    // 5. Imprimir resultados
    println("Estudiantes aprobados: $nombresAprobados")
    println("Promedio de nota de aprobados: $promedioAprobados")

    println("\nListado agrupado:")
    agrupados.forEach { (aprobado, lista) ->
        val estado = if (aprobado) "Aprobados" else "Reprobados"
        println("\n$estado:")
        lista.forEach { println("- ${it.nombre} (${it.nota})") }
    }
}
