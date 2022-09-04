---
id: dbna5ho9r85lmb0etellr01
title: Python
desc: ""
updated: 1662281871638
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
