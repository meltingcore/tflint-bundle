# tflint-bundle

"Forked" from the [original](https://github.com/terraform-linters/tflint-bundle) 

A Docker image with TFLint and ruleset plugins for AWS, Azure and GCP

```console
docker pull ghcr.io/meltingcore/tflint-bundle
```

Bundled versions:

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
