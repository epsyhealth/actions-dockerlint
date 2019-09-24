# Docker Lint Action

This is a GitHub action for running `dockerfilelint` on docker files and annotating diffs with the linter output

## Example

```yaml
name: Lint
on: [push]
jobs:
  lint:
    runs-on: ubuntu-latest
    steps: 
    - name: Checkout
      uses: actions/checkout@master
    - name: lint
      uses: luke142367/Docker-Lint-Action@v0.2.7
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        TARGET: Dockerfile
```