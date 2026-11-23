# frankenphp-builds

Unofficial [FrankenPHP](https://github.com/php/frankenphp) binaries built against
several PHP versions, for [Mullion](https://github.com/anabiiil/mullion).

Official FrankenPHP releases embed a single PHP version each. This repository's
`Build` workflow builds the same upstream sources, with the upstream build
scripts, against each supported PHP branch:

| Platform | Asset |
|---|---|
| macOS Apple Silicon | `frankenphp-mac-arm64-php<x.y.z>` (static, upstream `build-static.sh`) |
| Windows x64 | `frankenphp-windows-x86_64-php<x.y.z>.zip` (upstream Windows build, official ZTS PHP from windows.php.net) |

Releases are named after the upstream tag (`v1.14.0`). The workflow runs weekly and
only builds combinations that are not published yet, so new FrankenPHP releases and
new PHP patch releases show up on their own. Every asset has a SHA-256 digest
and a GitHub build-provenance attestation:

```
gh attestation verify frankenphp-mac-arm64-php8.4.27 --repo anabiiil/frankenphp-builds
```

## Availability

Branches that fail to build on a platform are listed here.

FrankenPHP is MIT licensed, © Kévin Dunglas. PHP is under the PHP License.
