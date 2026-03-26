# Commercial Guidelines

## Intended Use

This repository is designed for production governance design, controlled workspace bootstrapping, and validator integration in commercial environments.

## Recommended Operating Controls

- enforce branch protection on `main`
- require pull request review for protected spec files
- require CI validation for example fixtures before merge
- tag all public releases (`vX.Y.Z`)
- maintain signed release notes and changelog traceability

## Change Governance

- create new versioned files for each release
- do not overwrite previous release specs in place
- keep EN/ZH versions aligned by version number
- keep references and legal notices updated per release

## Compliance & Risk Notes

- treat policy and change-control files as high-trust assets
- preserve append-only audit semantics in runtime workspaces
- document known limitations in release notes
