# Mimir rules Deploy Action

Github Action to deploy Mimir rules through `mimirtool`.

## Usage

Here is an example of how to use this action with a YAML rules file in your repo:

```yaml
name: Deploy
on:
  release:
    types: [ published ]

jobs:
  deployment:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: Deploy
      uses: casavo/action-mimir-rules-deploy@v1
      with:
        endpoint: https://mimir.my.tld
        namespace: my-namespace
        path: alerts/my_rules.yaml
```
