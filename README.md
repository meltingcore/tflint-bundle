# tflint-bundle

## Summary

"Forked" from the [original](https://github.com/terraform-linters/tflint-bundle) 
deprecated project and  generates a convenient Docker image with TFLint 
and ruleset plugins for AWS, Azure and GCP.

The current philosophy is to regularly build the image using the latest versions
so if you want to pin you should use a release tag (there is no `stable` image tag).

## To Be Done

Ultimately the workflow in this repo should be:
* automatically trigger image builds when one of the source repos has a new release
* that trigger should create a new release in this repo where the versions being
packaged are also auto added in the release's description and in the README.

## Disclaimer

All this is just stepping on the shoulders of these giants:
https://github.com/terraform-linters.
I am not taking credit on any of their work!

## Usage

```console
docker pull ghcr.io/meltingcore/tflint-bundle
```

## Bundled versions

| Package                | Version   |
|------------------------|-----------|
| TFLint                 | `v0.48.0` |
| tflint-ruleset-aws     | `v0.27.0` |
| tflint-ruleset-azurerm | `v0.25.1` |
| tflint-ruleset-google  | `v0.25.0` |

These ruleset plugins are installed manually. If you want to enable it, just set `enabled = true` without specifying the version.

```hcl
plugin "aws" { enabled = true }
plugin "azurerm" { enabled = true }
plugin "google" { enabled = true }
```
