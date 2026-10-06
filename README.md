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

cl-procgen, cl-constrained-delaunay, common-shapes, HarfArasta, cl-earcut, cl-transitions, cl-dear-imgui[^2], cl-nuklear, cl-webgpu, cl-wuffs, trivial-high-precision-timer, lasm, miao, meow, trivial-simd.

Only git tags are released; commits are not.

[^1]: ql-https needs `curl`. Set `ql-https:*quietly-use-https*` to `t` to skip its retry prompt. Its installer replaces the Quicklisp setup in your init file; follow its README.
[^2]: The dist archive has no git submodules, so cl-dear-imgui needs a recursive clone.
