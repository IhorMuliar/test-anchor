# Test Anchor

A fast and easy action for testing your Solana [Anchor](https://www.anchor-lang.com/) project.

## Usage

Here's an example workflow:

```yaml
name: example-workflow
on: [push]
jobs:
  run-anchor-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: IhorMuliar/test-anchor@v1
```

This will use the default versions of Node.js, the Solana CLI tools and Anchor, which are 22.14.0, 2.2.3, and 0.31.0 respectively. You can also configure these versions like so:

```yaml
steps:
  - uses: actions/checkout@v4
  - uses: IhorMuliar/test-anchor@v1
    with:
      node-version: '22.14.0'
      solana-cli-version: '2.2.3'
      anchor-version: '0.31.0'
      workspace-dir: 'app'
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
