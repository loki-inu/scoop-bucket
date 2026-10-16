# loki-inu/scoop-bucket

[Scoop](https://scoop.sh) bucket for loki-inu tools on Windows.

## relnote

[relnote](https://github.com/loki-inu/relnote) turns a git range into clean GitHub release notes, or prepends a Keep a Changelog section to `CHANGELOG.md`. Pure standard-library Python, no config file, no GitHub API.

```powershell
scoop bucket add loki-inu https://github.com/loki-inu/scoop-bucket
scoop install loki-inu/relnote
relnote --help
```

relnote needs Python 3.11+ on `PATH`. If you don't have it yet:

```powershell
scoop install python
```

Usage:

```powershell
relnote                                   # notes since the latest tag
relnote --since v1.2.0 --until v1.3.0     # explicit range
relnote --next-version                    # suggest the next semver tag
relnote --changelog CHANGELOG.md --changelog-title v1.3.0
```

Docs: https://loki-inu.github.io/relnote/

The manifest installs the official single-file release (`relnote.pyz`) and checks it against the release `SHA256SUMS`. CI installs it with Scoop on Windows and generates notes from a test repo on every push.

## Other ways to install relnote

```bash
brew install loki-inu/tap/relnote
gh extension install loki-inu/gh-relnote
pip install git+https://github.com/loki-inu/relnote.git
```

## License

MIT
