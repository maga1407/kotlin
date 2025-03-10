#### ESTRUCTURA 1  
# MANEJO DE VARIABLES  

1. **Describa el por qué y para qué se utiliza.**
  El manejo de variable en Kotlin es muy importante porque es un lenguaje fuertemente tipado, lo que significa que cada variable tiene un tipo especifico:

- Int: Se utliza para números enteros.
- Double: Se utliza para números decimales mas grandes.
- Float: Se utiliza para números decimales mas cortos o menos presición.
- Boolean: Se utiliza para valores logicos (True -  False).
- Char: Se utliza para un solo caracter.
- String: Se utliza para cadenas de textos.

Se declaran con val para variables inmutables o var para variables mutables.

   
3. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  


🔗 **[LINK DE CODIGO](https://pl.kotl.in/SqckacgRi?readOnly=true)** 

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](#)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/maga1407/kotlin/blob/main/variables.png)**  

---

### Escribe una nota del cómo funciona la estructura  

fun main() {
    // Variables mutables (pueden cambiar de valor)
    var nombre: String = "Juan"
    var edad: Int = 25
    var altura: Double = 1.75
    var esEstudiante: Boolean = true

    // Variables inmutables (no pueden cambiar de valor)
    val pais: String = "México"
    val pi: Float = 3.1416f

    // Imprimir los valores
    println("Nombre: $nombre")
    println("Edad: $edad años")
    println("Altura: $altura metros")
    println("Es estudiante: $esEstudiante")
    println("País: $pais")
    println("Valor de pi: $pi")

    // Modificando variables mutables
    nombre = "Carlos"
    edad = 30

    println("Nuevo nombre: $nombre")
    println("Nueva edad: $edad años")
}
