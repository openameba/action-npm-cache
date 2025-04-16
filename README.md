# action-npm-cache

save or restore npm cache

## How to use

```yaml
steps:
  - uses: actions/checkout@v4
  - uses: actions/setup-node@v4
    with:
      node-version: lts/*
  - uses: openameba/action-npm-cache/restore@v1
  - run: npm test
  - if: github.ref_name == 'main'
    uses: openameba/action-npm-cache/save@v1
```
