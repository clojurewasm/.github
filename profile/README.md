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
  <a href="https://github.com/clojurewasm/Kiso"><img src="https://img.shields.io/github/stars/clojurewasm/Kiso?style=flat&label=Kiso&color=f7a41d" alt="Kiso stars"></a>
  <a href="https://github.com/zwasm/zwasm"><img src="https://img.shields.io/github/stars/zwasm/zwasm?style=flat&label=zwasm&color=f7a41d" alt="zwasm stars"></a>
</p>

---

> [!IMPORTANT]
> **These projects are no longer actively developed.** Building independent
> language runtimes from scratch turned out to be more than one person can
> sustain, so they stop here while they still work rather than eroding quietly.
>
> Everything stays **public** under its original licence — read it, fork it,
> rename it, build on it. No permission needed and no credit expected.
>
> The one thing that continues is **[zwasm](https://github.com/zwasm/zwasm)**,
> which has moved to its own organisation and is actively maintained there.

## Projects

### [ClojureWasm](https://github.com/clojurewasm/ClojureWasm) — a Clojure runtime in Zig

A from-scratch Clojure implementation with no JVM: a single small native binary
that starts in milliseconds, and a **WebAssembly FFI** that lets Clojure call
modules compiled from Rust, Go, Zig or C as if they were ordinary functions.

**No longer maintained.**
[v1.10.1](https://github.com/clojurewasm/ClojureWasm/releases/tag/v1.10.1) is
the final release, and the released binaries stay up — `brew install
clojurewasm/tap/cljw` still works. The repository stays open and unarchived so
it remains forkable; Issues are off and Pull Requests will not be reviewed, but
[Discussions](https://github.com/clojurewasm/ClojureWasm/discussions) are open
and the [announcement](https://github.com/clojurewasm/ClojureWasm/discussions/15)
explains the wind-down. There are **no security fixes** — do not run it against
untrusted input.

### [Kiso](https://github.com/clojurewasm/Kiso) — a ClojureScript compiler in TypeScript

An experimental ClojureScript-to-JavaScript compiler plus the **su** component
framework, with zero dependencies. Archived.

### [ClojureWit](https://github.com/clojurewasm/ClojureWit) — Clojure to WebAssembly components

Compiling Clojure source into WIT-typed WebAssembly components. Archived.

## Moved on: zwasm

**[zwasm](https://github.com/zwasm/zwasm)** — the fast, spec-compliant
WebAssembly runtime in Zig that ClojureWasm embeds — left this organisation for
[its own](https://github.com/zwasm), where it **continues under active,
separate maintainership**. It is a standalone runtime useful well beyond
Clojure, with a JIT, AOT compilation, WASI 0.3 and the Component Model. If you
came here for the WebAssembly part, that is where to go — and where a bug
report can still be acted on.

## Also here

Two demo applications and a games collection — the Playground, the Bookshelf,
and cw-arcade — are archived and their hosted instances shut down. Their source
stays public: each built `cljw` from source in its `Dockerfile`, so they remain
a complete worked example of deploying this runtime end to end.

---

<p align="center">
  <em>Thanks to everyone who used these, reported differences, and contributed fixes.</em>
</p>
