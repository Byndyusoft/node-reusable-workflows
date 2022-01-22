# node-reusable-workflows

[![test](https://github.com/Byndyusoft/node-reusable-workflows/actions/workflows/test-myself.yaml/badge.svg?branch=master)](https://github.com/Byndyusoft/node-reusable-workflows/actions/workflows/test-myself.yaml)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

Reusable workflows for Node.js

## Requirements

- Node.js v14 LTS or later
- yarn

## Usage

### .github/workflows/test.yaml

```yaml
name: test

on:
  - push
  - pull_request

jobs:
  test:
    uses: Byndyusoft/node-reusable-workflows/.github/workflows/test.yaml@master
```

### .github/workflows/deploy.yaml

```yaml
name: deploy

on:
  - workflow_dispatch

jobs:
  deploy:
    uses: Byndyusoft/node-reusable-workflows/.github/workflows/deploy.yaml@master
    secrets:
      NPM_TOKEN: ${{ secrets.NPM_TOKEN }}
```

## Maintainers

- [@Byndyusoft/owners](https://github.com/orgs/Byndyusoft/teams/owners) <<github.maintain@byndyusoft.com>>
- [@Byndyusoft/team](https://github.com/orgs/Byndyusoft/teams/team)
- [@KillWolfVlad](https://github.com/KillWolfVlad)

## License

This repository is released under version 2.0 of the
[Apache License](https://www.apache.org/licenses/LICENSE-2.0).
