#### ESTRUCTURA 7
# LOOPERS

---

1. **Describa el por qué y para qué se utiliza.**

El uso de loops en Kotlin es fundamental para la iteración de bloques de código. Permiten ejecutar una sección de código varias veces sin necesidad de escribirlo manualmente, ahorrando tiempo y mejorando la eficiencia del programa.

Tipos de loops en Kotlin:

for: Se utiliza para iterar sobre rangos, listas o arreglos.

while: Se ejecuta mientras la condición especificada sea verdadera.

do-while: Similar a while, pero garantiza que el bloque de código se ejecute al menos una vez.

Las estructuras de bucles ayudan a recorrer estructuras de datos, automatizar tareas repetitivas y mejorar la legibilidad del código.

---
   
2. **Genere un ejemplo internamente en el recuadro.**  

 ```kotlin
fun main() {
   for (i in 1..5) {
      println(i)
   }
  
  for (i in 0..10 step 2) {
   println(i)
   }
  
   for (i in 10 downTo 0) {
      println(i)
   }
    
   
   val numeros: Array<Int> = arrayOf (60, 2, 3, 4, 5)
    
   for (elem in numeros) {
      println(elem)
   }

   var i = 1
   while (i <= 5) {
      println(i)
      i = i + 1
   }

   var i = 1
   do {
      println(i)
      i++
   } while (i <= 5)
}
```
    

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/maga1407/kotlin/blob/main/loopers/loopers.mp3)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/maga1407/kotlin/blob/main/loopers/Loopers.png)**

---

3. **Escribe una nota del cómo funciona la estructura.**

```kotlin
   fun main() {
    // Ejemplo de for loop que recorre una lista de nombres
    val nombres = listOf("Ana", "Juan", "Carlos")
    for (nombre in nombres) // Cada elemento en la lista nombres {
        println("Nombre: $nombre") // Imprime cada nombre de la lista
    }

    // Ejemplo de while loop que cuenta hasta 3
    var contador = 1
    while (contador <= 3) //Mientras el contador sea menor o igual a 3 {
        println("Contador: $contador") // Muestra el valor del contador
        contador++ // Incrementa el contador
    }

    // Ejemplo de do-while loop que imprime números hasta que llegue a 0
    var numero = 3
    do {
        println("Número actual: $numero") // Muestra el número actual
        numero-- // Reduce el número en 1
    } while (numero > 0) // si el numero es mayor a 0 vuelve a empezar el bucle
}

```
