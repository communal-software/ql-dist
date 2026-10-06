# ql-dist

takeiteasy's [Quicklisp](https://www.quicklisp.org/) dist, built by [gh-ql-dist](https://github.com/takeiteasy/gh-ql-dist).

## Install

The dist is served over HTTPS. Stock Quicklisp only fetches `http://`, so it needs [ql-https](https://github.com/rudolfochrist/ql-https) first[^1]:

```lisp
(ql-dist:install-dist "https://takeiteasy.github.io/ql-dist/dist/takeiteasy.txt")
(ql:quickload :cl-earcut)
```

Without ql-https, clone the project into `~/quicklisp/local-projects/` instead.

## Projects

Only git tags are released; commits are not.

| Project | Description | Releases |
|---|---|---|
| [cl-procgen](https://github.com/takeiteasy/cl-procgen) | Procedural generation: noise, fBm, cellular automata, Poisson disc sampling | [cl-procgen](https://github.com/takeiteasy/ql-dist/releases?q=cl-procgen) |
| [cl-constrained-delaunay](https://github.com/takeiteasy/cl-constrained-delaunay) | Constrained Delaunay triangulation using a quad-edge data structure | [cl-constrained-delaunay](https://github.com/takeiteasy/ql-dist/releases?q=cl-constrained-delaunay) |
| [common-shapes](https://github.com/takeiteasy/common-shapes) | Triangle meshes for 2D and 3D shapes | [common-shapes](https://github.com/takeiteasy/ql-dist/releases?q=common-shapes) |
| [HarfArasta](https://github.com/takeiteasy/HarfArasta) | Text shaping and rendering (2D and 3D) via HarfBuzz | [HarfArasta](https://github.com/takeiteasy/ql-dist/releases?q=HarfArasta) |
| [cl-earcut](https://github.com/takeiteasy/cl-earcut) | Ear-clipping polygon triangulation with hole bridging and z-order hashing | [cl-earcut](https://github.com/takeiteasy/ql-dist/releases?q=cl-earcut) |
| [cl-transitions](https://github.com/takeiteasy/cl-transitions) | Finite state machines, a port of pytransitions | [cl-transitions](https://github.com/takeiteasy/ql-dist/releases?q=cl-transitions) |
| [cl-dear-imgui[^2]](https://github.com/takeiteasy/cl-dear-imgui) | CFFI bindings for Dear ImGui (dcimgui) | [cl-dear-imgui](https://github.com/takeiteasy/ql-dist/releases?q=cl-dear-imgui) |
| [cl-nuklear](https://github.com/takeiteasy/cl-nuklear) | CFFI/ECL bindings for the Nuklear immediate-mode GUI library | [cl-nuklear](https://github.com/takeiteasy/ql-dist/releases?q=cl-nuklear) |
| [cl-webgpu](https://github.com/takeiteasy/cl-webgpu) | FFI bindings and wrapper for WebGPU via wgpu-native, with a WGSL DSL | [cl-webgpu](https://github.com/takeiteasy/ql-dist/releases?q=cl-webgpu) |
| [cl-wuffs](https://github.com/takeiteasy/cl-wuffs) | Bindings for Wuffs: image decoding, ZIP, checksums, decompression | [cl-wuffs](https://github.com/takeiteasy/ql-dist/releases?q=cl-wuffs) |
| [trivial-high-precision-timer](https://github.com/takeiteasy/trivial-high-precision-timer) | Cross-platform high-precision timer | [trivial-high-precision-timer](https://github.com/takeiteasy/ql-dist/releases?q=trivial-high-precision-timer) |
| [lasm](https://github.com/takeiteasy/lasm) | DSL for building fantasy assemblers and CPU emulators | [lasm](https://github.com/takeiteasy/ql-dist/releases?q=lasm) |
| [miao](https://github.com/takeiteasy/miao) | Agent core built on meow, for building agent harnesses | [miao](https://github.com/takeiteasy/ql-dist/releases?q=miao) |
| [meow](https://github.com/takeiteasy/meow) | Plugin and service core: mount everything, order whenever | [meow](https://github.com/takeiteasy/ql-dist/releases?q=meow) |
| [trivial-simd](https://github.com/takeiteasy/trivial-simd) | Bulk SIMD arithmetic and BLAS for float and integer vectors | [trivial-simd](https://github.com/takeiteasy/ql-dist/releases?q=trivial-simd) |

[^1]:

```lisp
(ql-dist:install-dist "https://takeiteasy.github.io/ql-dist/dist/takeiteasy.txt")
(ql:quickload :cl-earcut)
```

Without ql-https, clone the project into `~/quicklisp/local-projects/` instead.

## Projects

cl-procgen, cl-constrained-delaunay, common-shapes, HarfArasta, cl-earcut, cl-transitions, cl-dear-imgui[^2], cl-nuklear, cl-webgpu, cl-wuffs, trivial-high-precision-timer, lasm, miao, meow, trivial-simd.

Only git tags are released; commits are not.

[^1]: ql-https needs `curl`. Set `ql-https:*quietly-use-https*` to `t` to skip its retry prompt. Its installer replaces the Quicklisp setup in your init file; follow its README.
[^2]: The dist archive has no git submodules, so cl-dear-imgui needs a recursive clone.
