# Antora Build action

This action builds an asciidoc based documentation with the antora documentation framework.

## Inputs

### `playbook`

**Optional** The name of the playbook to run. Default `"antora-playbook.yml"`.

## Example usage

Build the documentation with the default playbook.

``` yml
uses: rgn/antora-build-action@v1
```

Build the documentation with the production playbook.

``` yml
uses: rgn/antora-build-action@v1
with:
  playbook: 'antora-playbook.prd.yml'
```

Build the documentationw with private repostiories.

``` yml
uses:
with:
  playbook: '<yourplaybook.yml>'
env:
  GIT_CREDENTIALS: ${{secrets.GIT_CREDENTIALS}}
```
