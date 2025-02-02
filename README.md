# MiSTer-build-db github action

This action is for distributing assets targeted at the MiSTer platform.

## Usage

### Inputs

- db-name - Name of DB (value used by downloader)
- dryrun - Boolean flag to skip commiting

### Example

Create a file at `.github/workflows/build-db.yml` with the following content.

```yml
name: Build Custom Database

on:
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  build_db:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Build Custom Database for MiSTer Downloader
        uses: diegofigs/MiSTer-build-db@v1
        with:
          db-name: "your-db-name-here"
```
