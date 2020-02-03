# Gatsby

## Deployment via Github Actions

with e.g. https://github.com/enriikke/gatsby-gh-pages-action

File `.github/workflows/main.yml`

```yaml
name: CI

on:
  push:
    branches:
      - source

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v1
      - uses: enriikke/gatsby-gh-pages-action@v2
        with:
          access-token: ${{ secrets.ACCESS_TOKEN }}
```
