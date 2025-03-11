
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

🔗 **[LINK DEL AUDIO](https://github.com/user-attachments/assets/f3d8352b-d68a-4672-b5d7-37689effce86)**  
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


#### ESTRUCTURA 2  
# OPERADORES MATEMATICOS LOGICOS

1. **Describa el por qué y para qué se utiliza.**
  En Kotlin, los operadores matemáticos y lógicos son esenciales para realizar operaciones aritméticas y de comparación.

- Suma (+)
- Resta (-)
- Multiplicación (*)
- División (/)
- Modulo (%)

**OPERADORES DE ASIGANCIÓN**
- (+=)
- (-=)
- (*=)
- (/=)
- (%=)

**OPERADORES DE COMPARACIÓN**
- Igual a (==)
- Diferente de (!=)
- Mayor que (>)
- Menor que (<)
- mayor o igual que (>=)
- menor o igual que (<=)

**OPERADORES LÓGICOS**
- AND (&&)
- NOT (!)
- OR (||)

3. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

fun main() {
    
    val a = 10
    val b = 3
    
    println("Suma : ${a + b}")
    println("Resta : ${a - b}")
    println("Multiplicacion : ${a * b}")
    println("Division : ${a / b}")
    println("Modulo : ${a % b}")
    
    var x = 5
    println("x antes : $x")
    x += 2
    println("x despues de x +=2: $x")
    
    println("comparacion (a>b): ${a>b}")
    println("logica(true&&false): ${true&&false}")

}

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](#)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](#)**  

---

### Escribe una nota del cómo funciona la estructura  

fun main() {
    // Operadores Matemáticos
    val a = 10
    val b = 5
    println("Suma: ${a + b}")
    println("Resta: ${a - b}")
    println("Multiplicación: ${a * b}")
    println("División: ${a / b}")
    println("Módulo: ${a % b}")

    // Operadores de Asignación
    var c = 20
    c += 5  // Equivale a: c = c + 5
    println("Asignación con suma: $c")
    c -= 5  // Equivale a: c = c - 5
    println("Asignación con resta: $c")
    c *= 2  // Equivale a: c = c * 2
    println("Asignación con multiplicación: $c")
    c /= 2  // Equivale a: c = c / 2
    println("Asignación con división: $c")
    c %= 3  // Equivale a: c = c % 3
    println("Asignación con módulo: $c")

    // Operadores de Comparación
    println("¿a es igual a b?: ${a == b}")
    println("¿a es diferente de b?: ${a != b}")
    println("¿a es mayor que b?: ${a > b}")
    println("¿a es menor que b?: ${a < b}")
    println("¿a es mayor o igual que b?: ${a >= b}")
    println("¿a es menor o igual que b?: ${a <= b}")

    // Operadores Lógicos
    val x = true
    val y = false
    println("AND lógico (true && false): ${x && y}")
    println("OR lógico (true || false): ${x || y}")
    println("NOT lógico (!true): ${!x}")
}
