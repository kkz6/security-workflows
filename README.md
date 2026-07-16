# Security workflows

Reusable security scanning for repositories owned by `kkz6`.

The central workflow blocks on focused rules for obfuscated executable payloads
in JavaScript and TypeScript project configuration files. Semgrep's broader
community security audit runs in advisory mode because framework-specific code
can produce findings that need human review. Repository secret scanning remains
GitHub's responsibility to avoid blocking on known fixture hashes and other
non-secret test data.

Caller repositories use:

```yaml
jobs:
  security:
    uses: kkz6/security-workflows/.github/workflows/semgrep.yml@main
```

The container image and GitHub Actions are pinned to immutable digests or
commit SHAs. Update these references deliberately through reviewed changes.
