#### ESTRUCTURA 3
# Funciones de Strings y Printing

---

1. **Describa el por qué y para qué se utiliza.**  
   En Kotlin, las estructuras de Strings e Printing son fundamentales para manejar y mostrar texto en programas.

   **Cadenas en Kotlin (String)**  
   Un String es una secuencia de caracteres. En Kotlin, las cadenas son objetos inmutables de la clase `String`, lo que significa que su contenido no puede cambiar después de su creación.

   - Se pueden definir con comillas dobles `"`.
   - Admiten interpolación de variables y expresiones.

   **Impresión en Kotlin (Printing)**  
   La impresión en Kotlin se usa para mostrar información en la consola.

   Funciones principales para imprimir en Kotlin:
   - `print()`: Muestra un mensaje en la consola sin salto de línea.
   - `println()`: Muestra un mensaje en la consola con un salto de línea al final.

---

2. **Genere un ejemplo internamente en el recuadro.**  
   Utilice un editor de código para lograrlo.

   🔗 **[LINK DE CÓDIGO](https://pl.kotl.in/seEykWcuq?readOnly=true)**

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO]()**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB]()**

---

### Escribe una nota del cómo funciona la estructura 

```kotlin
fun main() {
    // Definimos una variable con un mensaje simple
    val mensaje: String = "Bienvenido a Kotlin avanzado"

    // Imprimimos el mensaje almacenado en la variable
    println(mensaje) // Salida: Bienvenido a Kotlin avanzado

    // Concatenación de cadenas usando el operador +
    val nombre = "Carlos"
    val saludo = "Hola, " + nombre + "!" // Se concatena "Hola, " con el valor de la variable nombre
    println(saludo) // Salida: Hola, Carlos!

    // Uso de interpolación de cadenas con $
    val edad = 30
    println("Carlos tiene $edad años") // Salida: Carlos tiene 30 años

    // Uso de expresiones dentro de interpolación
    println("En 5 años, Carlos tendrá ${edad + 5} años") // Se evalúa edad + 5 antes de imprimir

    // Cadena multilínea con triple comillas
    val descripcion = """
        Kotlin es un lenguaje moderno
        con tipado fuerte y seguro.
        Soporta programación funcional y orientada a objetos.
    """.trimIndent() // trimIndent elimina espacios innecesarios al inicio de cada línea
    println(descripcion)

    // Uso de caracteres de escape
    println("Carlos dijo: \"Kotlin es genial!\"") // Se usa \" para incluir comillas en el string

    // Imprimir caracteres especiales con \n para salto de línea y \t para tabulación
    println("Lista de tareas:\n\t1. Aprender Kotlin\n\t2. Practicar código\n\t3. Crear proyectos")

    // Repetir una cadena varias veces
    val repeticion = "Kotlin! ".repeat(3) // "Kotlin! " se repite 3 veces
    println(repeticion) // Salida: Kotlin! Kotlin! Kotlin! 

    // Obtener caracteres individuales de una cadena
    val palabra = "Programación"
    println("La primera letra de '$palabra' es '${palabra[0]}'") // Se accede al primer carácter

    // Obtener el tamaño de una cadena
    println("La palabra '$palabra' tiene ${palabra.length} letras") // length obtiene el tamaño

    // Reemplazo de caracteres en una cadena
    val fraseOriginal = "Me gusta Java"
    val fraseNueva = fraseOriginal.replace("Java", "Kotlin") // Reemplaza "Java" por "Kotlin"
    println(fraseNueva) // Salida: Me gusta Kotlin
}