#### ESTRUCTURA 5
# Estructuras de Decisión, Control y Manejo de Errores en Kotlin

---

## 1. **Describa el por qué y para qué se utiliza**

En Kotlin, el control de flujo se divide en tres categorías principales:

### 1️⃣ Estructuras de Decisión → Elegir qué código ejecutar
#### `if-else` (Decisión Simple y Compuesta)
- **¿Por qué?** Para evaluar condiciones booleanas
- **¿Para qué?** 
  - Verificar si una persona puede votar
  - Controlar acceso a contenido restringido
  - Validar datos de entrada

#### `when` (Similar a `switch` en otros lenguajes)
- **¿Por qué?** Evita múltiples `if-else` anidados
- **¿Para qué?**
  - Evaluar días de la semana
  - Manejar estados de usuario
  - Procesar diferentes tipos de cuenta

### 2️⃣ Estructuras de Control → Ejecución repetitiva
#### `for` (Bucle con rango o lista)
- **¿Por qué?** Optimiza iteraciones sobre colecciones
- **¿Para qué?**
  - Recorrer arrays/listas
  - Generar secuencias numéricas
  - Procesar elementos de conjuntos

#### `while` (Bucle condicional)
- **¿Por qué?** Cuando no se conoce el número de iteraciones
- **¿Para qué?**
  - Validar contraseñas
  - Esperar respuestas de servidor
  - Procesar streams de datos

#### `do-while` (Bucle con ejecución mínima)
- **¿Por qué?** Garantiza al menos una ejecución
- **¿Para qué?**
  - Validar formularios
  - Generar números aleatorios
  - Menús interactivos

### 3️⃣ Manejo de Errores → Gestionar excepciones
#### `try-catch` (Control de excepciones)
- **¿Por qué?** Previene cierres abruptos
- **¿Para qué?**
  - Conversión de tipos
  - Operaciones matemáticas inválidas
  - Acceso a recursos externos

#### `try-catch-finally` (Bloque de limpieza)
- **¿Por qué?** Ejecuta código esencial siempre
- **¿Para qué?**
  - Liberar memoria
  - Cerrar archivos/conecciones
  - Guardar estados finales

#### `throw` (Excepciones personalizadas)
- **¿Por qué?** Para reglas de negocio específicas
- **¿Para qué?**
  - Validar edad mínima
  - Verificar saldos suficientes
  - Controlar permisos de usuario

---
2. **Genere un ejemplo internamente en el recuadro.**  
   Utilice un editor de código para lograrlo.

   🔗 **[LINK DE CÓDIGO](https://pl.kotl.in/wDk_zGrtn?readOnly=true)**

### EN EL LISTADO COMPARTIDO BUSQUE EL ALGORITMO QUE CORRESPONDA Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO]()**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB]()**

---

### Escribe una nota del cómo funciona la estructura 

```kotlin
fun main() {
   // 1️⃣ if-else
   val numero = 15
   println(if (numero % 2 == 0) "Par" else "Impar")

   // 2️⃣ when
   when (readLine()?.toIntOrNull()) {
      1 -> println("Opción 1")
      2 -> println("Opción 2")
      else -> println("Inválido")
   }

   // 3️⃣ for
   (1..5).forEach { println("Iteración $it") }

   // 4️⃣ while
   var contador = 3
   while (contador-- > 0) println("Countdown: $contador")

   // 5️⃣ do-while
   do {
      println("Este mensaje aparece al menos una vez")
   }  while (false)

   // 6️⃣ break/continue
   for (i in 1..10) {
      if (i == 5) continue
      if (i == 8) break
      println("Número $i")
    }

   // 7️⃣ try-catch
   try {
      println(10 / readLine()!!.toInt())
   }  catch (e: Exception) {
      println("Error: ${e.message}")
   }  finally {
      println("Operación finalizada")
   }

   // 8️⃣ throw
   val edad = 16
   if (edad < 18) throw Exception("Menor de edad")
}