# Get The Default Branch Action

This action is for getting the default branch.

# Examples

You can use the test workflow in `.github/workflows/main.yml` as a starting point.

```yaml
jobs:
  test_action:
    runs-on: ubuntu-latest
    name: Make sure the action works
    steps:
      - uses: actions/checkout@v2
      - id: default-branch
        uses: scottmmjackson/get-the-default-branch-action@v1
      - if: ${{ steps.default-branch.outputs.default_branch == 'main' }}
        run: echo "Success! The default branch is in fact 'main'!"
```

Enjoy!