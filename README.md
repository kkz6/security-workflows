# Security workflows

Reusable security scanning for repositories owned by `kkz6`.

The central workflow runs Semgrep's security and secret rules alongside local
rules for obfuscated executable payloads in JavaScript and TypeScript project
configuration files.

Caller repositories use:

```yaml
jobs:
  security:
    uses: kkz6/security-workflows/.github/workflows/semgrep.yml@main
```

The container image and GitHub Actions are pinned to immutable digests or
commit SHAs. Update these references deliberately through reviewed changes.
