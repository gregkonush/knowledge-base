
## Code snippet for JavaScript execution with GraalVM


```kotlin
import org.graalvm.polyglot.Context
import org.graalvm.polyglot.Value

fun main() {
  Context.create().use { context ->
    val function: Value = context.eval("js", """
      (
        function square(param) {
          return param * param;
        }
      )
    """.trimIndent())
    assert(function.canExecute())
    val x: Int = function.execute(41).asInt()
    println(x)
  }
}
```
