---
id: uic6mk01wqhr5vtwcqd3tj8
title: Graalvm
desc: ''
updated: 1662242158872
created: 1662241748417
---

## Code snippets for JavaScript execution with GraalVM


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
