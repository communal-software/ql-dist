# Maintaining the dist

`projects.txt` lists public Lisp repositories and their tag selectors. A manifest push rebuilds the dist; project tag notifiers trigger updates after releases.

## Visibility audit

Check every manifest repository's GitHub visibility before adding it. Private repositories do not belong in the public dist. Remove their manifest entries and delete their existing dist release archives and tags.

Public projects need a top-level ASDF system with a version and a matching git tag. Keep the [project table](projects.md) synchronized with the manifest.

## Release notifications

Each project has `.github/workflows/ql-dist.yml` and a `QL_DIST_TOKEN` secret restricted to this dist repository. The dist enables repository dispatch through `QL_DIST_DISPATCH=true`; nightly polling is disabled.

Push project branches and tags to GitHub and sourcehut. Verify the notifier, dist workflow, release assets and Pages metadata after an update.

## Historical metadata

The current dist indexes contain only allowlisted projects. Historical metadata is retained, but private-project archives and release tags are removed. Existing installations using those historical private archives cannot download them.
