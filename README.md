[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/msudgh/actions-npm-check-updates?style=social)](
  https://github.com/msudgh/actions-npm-check-updates/releases
)
[![MIT License](https://img.shields.io/badge/license-MIT-brightgreen?style=social)](
  https://mit-license.org/msudgh
)

Create pull requests for the latest version of NPM packages

## Usage
Here is an example workflow to update NPM packages with scheduled runs:

```yaml
name: Update NPM packages

on:
  # Allow manual triggers.
  workflow_dispatch:

  # Automatically run once a week.
  schedule:
    - cron: "0 0 1 * SAT"

jobs:
  update-packages:
    runs-on: ubuntu-latest
    steps:
      - name: Update packages
        uses: msudgh/actions-npm-check-updates@v0.1.0
```
