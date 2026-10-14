# ql-dist

communal-software's public [Quicklisp](https://www.quicklisp.org/) dist, built by [gh-ql-dist](https://github.com/takeiteasy/gh-ql-dist).

[Projects](docs/projects.md) · [Maintaining the dist](docs/maintenance.md)

## Install

Install [ql-https](https://github.com/rudolfochrist/ql-https) first; stock Quicklisp only fetches HTTP.[^https]

```lisp
(ql-dist:install-dist "https://communal-software.github.io/ql-dist/dist/communal-software.txt")
(ql:quickload :cl-inference)
```

Without ql-https, clone a project into `~/quicklisp/local-projects/` instead.

[^https]: ql-https needs `curl`. Set `ql-https:*quietly-use-https*` to `t` to skip its retry prompt. Its installer replaces the Quicklisp setup in your init file; follow its README.
