#### ESTRUCTURA 4
# CONTROL DE FLUJO

---

1. **Describa el por qué y para qué se utiliza.**

El control de flujo en Kotlin permite ejecutar diferentes bloques de código según condiciones o repeticiones. Existen tres tipos principales: condicionales, bucles e instrucciones de salto.

1. Condicionales (if, when)
Permiten ejecutar código basado en condiciones.

2. Bucles (for, while, do-while)
Permiten repetir un bloque de código.

3. Instrucciones de salto (break, continue, return)

---
   
2. **Genere un ejemplo internamente en el recuadro.**  

   - Utilice un editor de código para lograrlo.  

🔗 **[LINK DE CODIGO](https://pl.kotl.in/DqChlDrJG?readOnly=true)** 

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO]()**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](<img width="243" alt="estructurascontrol" src="https://github.com/user-attachments/assets/529460ef-5e10-4bd5-a383-6be71de91a65" />
)**

``kotlin

fun main() {
    // Lista de invitados al evento
    val listaInvitados = listOf("Ana", "Juan", "Pedro", "María")

    // Cupo disponible para el evento
    var cupoDisponible = 3

    // Datos del usuario que intenta ingresar
    val nombreUsuario = "Juan"
    val edadUsuario = 19

    // Verificamos si la persona está en la lista de invitados
    if (nombreUsuario in listaInvitados) {
        println("Bienvenido, $nombreUsuario. Verificando acceso...")

        // Verificamos si la edad es suficiente
        if (edadUsuario >= 18) {
            println("Edad válida. Verificando cupo...")

            // Verificamos si hay cupo disponible
            if (cupoDisponible > 0) {
                println("Acceso concedido. ¡Disfruta del evento!")
                cupoDisponible-- // Reducimos el cupo en 1
            } else {
                println("Lo sentimos, no hay cupos disponibles.")
            }
        } else {
            println("Acceso denegado. Debes ser mayor de edad.")
        }
    } else {
        println("Lo sentimos, $nombreUsuario. No estás en la lista de invitados.")
    }

    // Bucle para mostrar cuántos cupos quedan disponibles
    println("Cupos restantes:")
    for (i in cupoDisponible downTo 1) {
        println("Cupo $i disponible")
    }

    // Evaluación de mensaje según cupo restante usando when
    when (cupoDisponible) {
        3 -> println("El evento está vacío.")
        in 1..2 -> println("Aún hay cupos disponibles.")
        0 -> println("Evento lleno. No hay más cupos.")
    }
}

