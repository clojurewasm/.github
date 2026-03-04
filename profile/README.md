<h1 align="center">
  <br>
  <code>(clojure × wasm)</code>
  <br>
</h1>

<p align="center">
  <strong>Clojure beyond the JVM — native binaries, WebAssembly, instant startup.</strong>
</p>

<p align="center">
  <a href="https://github.com/clojurewasm/ClojureWasm"><img src="https://img.shields.io/github/stars/clojurewasm/ClojureWasm?style=flat&label=ClojureWasm&color=f7a41d" alt="ClojureWasm stars"></a>
  <a href="https://github.com/clojurewasm/zwasm"><img src="https://img.shields.io/github/stars/clojurewasm/zwasm?style=flat&label=zwasm&color=f7a41d" alt="zwasm stars"></a>
  <a href="https://github.com/sponsors/chaploud"><img src="https://img.shields.io/github/sponsors/chaploud?logo=githubsponsors&logoColor=white&color=ea4aaa" alt="Sponsors"></a>
</p>

---

We build **independent language runtimes in Zig** — from-scratch implementations focused on fast startup, small binaries, and deep WebAssembly integration.

## Projects

### [ClojureWasm](https://github.com/clojurewasm/ClojureWasm) — Clojure Runtime in Zig

A full-scratch Clojure implementation. No JVM, no transpilation.

- ~**4 ms** startup / ~**4 MB** binary (single executable)
- **1,130+ vars** across 30+ namespaces (651/706 clojure.core)
- Dual backend: bytecode VM (with ARM64 JIT) + TreeWalk interpreter
- deps.edn compatible (git deps, local deps, aliases)
- nREPL server with CIDER support
- `cljw build app.clj -o app` — standalone binary, no runtime needed

### [zwasm](https://github.com/clojurewasm/zwasm) — WebAssembly Runtime in Zig

A fast, spec-compliant WebAssembly runtime.

- Full **Wasm 3.0** support (all 9 proposals including GC, SIMD, exception handling)
- **523 opcodes** (236 core + 256 SIMD + 31 GC)
- Register IR with **ARM64 / x86_64 JIT**
- Wins **14/23** benchmarks vs wasmtime, with **~43x smaller** binary
- WASI support (file I/O, clock, random, args, environ)

### Kiso — ClojureScript Compiler in TypeScript *(coming soon)*

A ClojureScript-to-JavaScript compiler. Early stage.

## Get Involved

- Try it: `zig build && ./zig-out/bin/cljw -e '(println "hello")'`
- Report issues on each project's repository
- [Sponsor development](https://github.com/sponsors/chaploud)

<p align="center"><sub>ClojureWasm: <a href="https://www.eclipse.org/legal/epl-v10.html">EPL-1.0</a> / zwasm: <a href="https://opensource.org/licenses/MIT">MIT</a></sub></p>
