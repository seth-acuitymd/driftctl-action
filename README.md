# GitHub Action for driftctl

## This project was forked from `snyk/driftctl-action` which is now in maintenance mode

## I ([seth](https://github.com/seth-acuitymd)) am going to see if I can get this project moving again, at least for my own use

The fork for `driftctl` itself is here: [seth-acuitymd/driftctl](https://github.com/seth-acuitymd/driftctl)

## `driftctl-action`

`driftctl-action` runs a full driftctl scan in your GitHub Actions workflow.

## Inputs

### `version`

The version of driftctl to install. Default to `latest`.

### `args`

A single string containing any additional arguments or flags to supply to the `scan` command. Defaults to an empty string.

## Example usage

```yml
name: Test Workflow

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Run driftctl
        uses: snyk/driftctl-action@v1
        with:
          version: 0.38.2
```

### How to Contribute

Should you wish to make a contribution please open a pull request against this repository with a clear description of the change with tests demonstrating the functionality.
