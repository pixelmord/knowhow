# Start a new project

// Last modified: 2020/04/03 09:24:50

## Steps

### Clone or `npm init -y`

### copy common files

1. editorconfig
2. prettier.config
3. LICENSE file

### Install and configure semantic release

#### Add config to `package.json`

```json
{
  "release": {
    "branch": "master",
    "plugins": [
      "@semantic-release/commit-analyzer",
      "@semantic-release/release-notes-generator",
      "@semantic-release/changelog",
      "@semantic-release/github",
      [
        "@semantic-release/git",
        {
          "assets": ["CHANGELOG.md"],
          "message": "chore(release): ${nextRelease.version} \n\n${nextRelease.notes}"
        }
      ]
    ]
  }
}
```

#### Install dependencies

```bash
yarn add --dev semantic-release @semantic-release/commit-analyzer @semantic-release/release-notes-generator @semantic-release/changelog @semantic-release/github @semantic-release/git
```

#### Add a Github Action

See [release.yml](../.github/workflows/release.yml)

### Setup commit linting

Install husky and commitlint:

```bash
yarn add --dev husky @commitlint/{config-conventional,cli}
```

Amend package.json:

```json
{
  "husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  }
}
```

Add [commitlint.config](../commitlint.config.js)
