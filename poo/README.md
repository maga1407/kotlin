#### ESTRUCTURA 10
# POO  

---

1. **Describa el por qué y para qué se utiliza.**

Se utiliza para organizar y estructurar mejor el código, especialmente cuando los programas crecen y se vuelven más complejos.

¿Por qué se utiliza?

Permite dividir el código en clases y objetos, lo que hace que sea más fácil de leer y mantener.Se pueden crear clases reutilizables que se pueden instanciar varias veces con diferentes valores. Es más fácil escalar y añadir nuevas funcionalidades sin romper lo que ya funciona. Localizar errores o hacer mejoras es más fácil cuando el código está organizado en objetos y clases. Ayuda a representar elementos del mundo real (como “Usuario”, “Producto”, “Pedido”, etc.) directamente en el código.

¿Para qué se utiliza?

Definir clases que representen entidades (por ejemplo, una clase Persona con propiedades como nombre y edad). Crear objetos que son instancias de esas clases (como val p = Persona("Isabella", 20)). Encapsular datos usando private, protected y public para controlar el acceso a las propiedades o funciones. Usar herencia para que una clase hija herede de una clase padre (open class Animal → class Perro : Animal()). Aplicar polimorfismo, que permite usar la misma interfaz o clase base para diferentes tipos de objetos. Dividir responsabilidades usando principios como SOLID, donde cada clase tiene una única responsabilidad.
---
   
2. **Genere un ejemplo internamente en el recuadro.**  

   - Utilice un editor de código para lograrlo.
  
```kotlin
abstract class Empleado(val nombre: String) {
    abstract fun trabajar()
}

class Programador(nombre: String): Empleado(nombre) {
    override fun trabajar() {
        println("👨‍💻 $nombre está programando en Kotlin.")
    }
}

class Diseñador(nombre: String): Empleado(nombre) {
    override fun trabajar() {
        println("🎨 $nombre está diseñando interfaces.")
    }
}

fun main() {
    val empleados: List<Empleado> = listOf(
        Programador("Ana"),
        Diseñador("Carlos"),
        Programador("Luis"),
        Diseñador("Lorena")
    )

    for (empleado in empleados) {
        empleado.trabajar()
    }
}
```
   

🔗 **[LINK DE CODIGO]()** 

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO]()**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB

---

3 .Escribe una nota del cómo funciona la estructura.


 ```kotlin

// 1. ABSTRACCIÓN
// Creamos una clase abstracta llamada 'Animal'.
// Esta clase representa cualquier tipo de animal y define lo esencial que todos deben tener.
abstract class Animal(private val nombre: String) {

    // 2. ENCAPSULAMIENTO
    // La propiedad 'nombre' es privada (no accesible desde fuera de la clase directamente),
    // lo que protege su valor. Solo se puede acceder a ella mediante este método.
    fun obtenerNombre(): String {
        return nombre
    }

    // Método abstracto: las clases hijas deben implementar su propia versión.
    // Esto obliga a cada tipo de animal a tener su propio sonido.
    abstract fun hacerSonido()
}

// 3. HERENCIA
// La clase 'Perro' hereda de 'Animal' usando dos puntos (:).
// Debe implementar el método abstracto 'hacerSonido'.
class Perro(nombre: String) : Animal(nombre) {
    override fun hacerSonido() {
        // Usamos el método obtenerNombre() para acceder al nombre, ya que 'nombre' es privado.
        println("${obtenerNombre()} dice: ¡Guau!")
    }
}

// Otra clase hija: 'Gato', también hereda de 'Animal'
class Gato(nombre: String) : Animal(nombre) {
    override fun hacerSonido() {
        println("${obtenerNombre()} dice: ¡Miau!")
    }
}

fun main() {
    // 4. POLIMORFISMO
    // Creamos una lista de tipo Animal, pero dentro ponemos objetos de tipo Perro y Gato.
    // Esto demuestra polimorfismo: una misma interfaz (Animal) con distintos comportamientos.
    val animales: List<Animal> = listOf(
        Perro("Rocky"),
        Gato("Misu"),
        Perro("Firulais")
    )

    // Recorremos la lista de animales
    for (animal in animales) {
        // Al llamar a hacerSonido(), cada objeto responde con su propia versión del método.
        // Esto es posible gracias al polimorfismo.
        animal.hacerSonido()
    }
}

```
