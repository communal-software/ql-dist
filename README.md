# ql-dist

A [Quicklisp](https://www.quicklisp.org/) dist built by [gh-ql-dist](https://github.com/takeiteasy/gh-ql-dist).

1. List projects in `projects.txt`.
2. Settings → Pages → Source: **GitHub Actions**.
3. Push.

```lisp
(ql-dist:install-dist "https://<owner>.github.io/<repo>/dist/<repo>.txt")
```

The dist is named after the repo; set the repo variable `QL_DIST_NAME` to change it.

Per-repo tag triggers and nightly polling are off by default: see [triggers](https://github.com/takeiteasy/gh-ql-dist/blob/main/docs/triggers.md).
