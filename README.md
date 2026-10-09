# ql-dist

communal-software's [Quicklisp](https://www.quicklisp.org/) dist, built by [gh-ql-dist](https://github.com/takeiteasy/gh-ql-dist).

## Install

The dist is served over HTTPS. Stock Quicklisp only fetches `http://`, so it needs [ql-https](https://github.com/rudolfochrist/ql-https) first[^1]:

```lisp
(ql-dist:install-dist "https://communal-software.github.io/ql-dist/dist/communal-software.txt")
(ql:quickload :cl-earcut)
```

Without ql-https, clone the project into `~/quicklisp/local-projects/` instead.

## Projects

Only git tags are released; commits are not.

| Project | Description |
|---|---|
| [cl-procgen](https://github.com/communal-software/cl-procgen) | Procedural generation: noise, fBm, cellular automata, Poisson disc sampling |
| [cl-constrained-delaunay](https://github.com/communal-software/cl-constrained-delaunay) | Constrained Delaunay triangulation using a quad-edge data structure |
| [cl-meshgen](https://github.com/communal-software/cl-meshgen) | Triangle meshes for 2D and 3D shapes |
| [HarfArasta](https://github.com/communal-software/HarfArasta) | Text shaping and rendering (2D and 3D) via HarfBuzz |
| [cl-earcut](https://github.com/communal-software/cl-earcut) | Ear-clipping polygon triangulation with hole bridging and z-order hashing |
| [cl-transitions](https://github.com/communal-software/cl-transitions) | Finite state machines, a port of pytransitions |
| [cl-dear-imgui](https://github.com/communal-software/cl-dear-imgui)[^2] | CFFI bindings for Dear ImGui (dcimgui) |
| [cl-nuklear](https://github.com/communal-software/cl-nuklear) | CFFI/ECL bindings for the Nuklear immediate-mode GUI library |
| [cl-webgpu](https://github.com/communal-software/cl-webgpu) | FFI bindings and wrapper for WebGPU via wgpu-native, with a WGSL DSL |
| [cl-wuffs](https://github.com/communal-software/cl-wuffs) | Bindings for Wuffs: image decoding, ZIP, checksums, decompression |
| [trivial-high-precision-timer](https://github.com/communal-software/trivial-high-precision-timer) | Cross-platform high-precision timer |
| [miao](https://github.com/communal-software/miao) | Agent core built on meow, for building agent harnesses |
| [meow](https://github.com/communal-software/meow) | Plugin and service core: mount everything, order whenever |
| [trivial-simd](https://github.com/communal-software/trivial-simd) | Bulk SIMD arithmetic and BLAS for float and integer vectors |
| [trivial-watch](https://github.com/communal-software/trivial-watch) | Cross-platform file and directory change notifications |

[^1]: ql-https needs `curl`. Set `ql-https:*quietly-use-https*` to `t` to skip its retry prompt. Its installer replaces the Quicklisp setup in your init file; follow its README.
[^2]: The dist archive has no git submodules, so cl-dear-imgui needs a recursive clone.
