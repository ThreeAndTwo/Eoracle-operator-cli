# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/Eoracle-operator-cli`
Branch: `develop`
Inspected head: `37ced49a1c718991bf11c7d861d8ccb6ede855fd`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/enforce_branch_name.yml` — original Git object `1055c1685eb002a16fce7bf5c90a52d66ea756b8`.
- `.github/workflows/operator_cli_build.yml` — original Git object `1b09a38ddd9c23217984be7553fb960cf24c0ab9`.
- `.github/workflows/release.yml` — original Git object `8b683632ab2bffb3d3d9f155b823f8408184e8cc`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
