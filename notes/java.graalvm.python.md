---
id: dbna5ho9r85lmb0etellr01
title: Python
desc: ""
updated: 1662329603250
created: 1662281688338
---

Arm chipped MacOS doesn't have a build for python intepreter in GraalVM

When I tried to list available packages

```bash
gu list
```

This didn't give any relevant results

Python is available in Linux

```bash
gu available
Downloading: Component catalog from www.graalvm.org
ComponentId              Version             Component name                Stability                     Origin
---------------------------------------------------------------------------------------------------------------------------------
espresso                 22.2.0              Java on Truffle               Supported                     github.com
espresso-llvm            22.2.0              Java on Truffle LLVM Java librSupported                     github.com
js                       22.2.0              Graal.js                      Supported                     github.com
llvm                     22.2.0              LLVM Runtime Core             Experimental                  github.com
llvm-toolchain           22.2.0              LLVM.org toolchain            Supported                     github.com
native-image             22.2.0              Native Image                  Early adopter                 github.com
nodejs                   22.2.0              Graal.nodejs                  Supported                     github.com
python                   22.2.0              Graal.Python                  Experimental                  github.com
R                        22.2.0              FastR                         Experimental                  github.com
ruby                     22.2.0              TruffleRuby                   Experimental                  github.com
visualvm                 22.2.0              VisualVM                      Experimental                  github.com
wasm                     22.2.0              GraalWasm                     Experimental                  github.com
```

It needs additional dependency: `llvm-toolchain`

So using IntelliJ didn't work out with WSL2
I can try to use vscode to compile and run simple code directly with kotlin compiler

```bash
# install
sdk install kotlin
# compile a file
kotlinc main.kt
# execute
kotlin MainKt.class

```

So it works with simple gradle setup, here is the snippet

```kotlin
import org.graalvm.polyglot.Context

fun main() {
  Context.create().use { context ->
    val function = context.eval("python", """
lambda total_units, price_per_unit: \
  total_units * price_per_unit if total_units < 1000 else \
    total_units * price_per_unit if total_units < 2000 else \
      50000
""");
    print(function.execute(1002, 1).asInt())
  }
}
```

