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

---

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

🔗 **[LINK DEL CODIGO](https://pl.kotl.in/flBVVF9sa?readOnly=true)**

---

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](#)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/user-attachments/assets/a07ff286-fb21-45c7-b0e6-a082a0c5be05)**  

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
