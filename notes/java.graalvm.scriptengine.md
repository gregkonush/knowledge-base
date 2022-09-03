---
id: d8t0fehrrlw5jnjugyk5l2a
title: Script Engine
desc: ''
updated: 1662247003066
created: 1662246966384
---

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
