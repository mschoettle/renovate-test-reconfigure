# MRE for discussion: 44808

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Then replace the current `h1` with the Renovate Issue/Discussion number.

## Current behavior

config-validator shows inconsistent results when using JSON5 or JSONC config

I created a branch `renovate/reconfigure` where I added a `renovate.json5` file. I use the `:enablePreCommit` preset. However, the Renovate comment explaining what will happen does not show that it is enabled and that I will get a PR for a pre-commit hook.

When the file is `renovate.json` it works. See this comment: [mschoettle/renovate-test-reconfigure#1 (comment)](https://github.com/mschoettle/renovate-test-reconfigure/pull/1#issuecomment-5061928798) (click on "edited" and the first entry, it will show the diff going from `.json` to `.json5`).

The problem also happens with `.jsonc` (noticed in a private repo).

## Expected behavior

The config validation should match what actually will happen and be consistent irregardless of the file name/extension.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/44808
