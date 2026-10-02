# Contributing to LastPing

Thanks for helping. LastPing is a hosted service at [lastping.dev](https://lastping.dev); the public repositories hold the pieces you run yourself.

## Where things go

| You want to... | Go to |
|---|---|
| Report a bug in the Terraform provider | [lastping-dev/terraform-provider-lastping issues](https://github.com/lastping-dev/terraform-provider-lastping/issues) |
| Report a bug in the `lastping` CLI or the MCP server binary | [tp322d/lastping-app issues](https://github.com/tp322d/lastping-app/issues) |
| Report a problem with the hosted service, the web app or the API | Email [hello@lastping.dev](mailto:hello@lastping.dev) |
| Report a security vulnerability | Do **not** open an issue. See [SECURITY.md](SECURITY.md). |
| Ask a usage question | See [SUPPORT.md](SUPPORT.md) |

Open the issue in the repository the problem lives in. If you are not sure which one that is, email us and we will route it.

## Reporting a bug

Search the open issues first. A useful report has:

- the version (`terraform version` and the provider version, or `lastping --version`)
- what you ran, with the smallest config or command that shows the problem
- what you expected, and what happened instead, including the full error text
- your OS and architecture if it is the CLI

Remove API keys (`lp_...`), webhook URLs and other credentials from anything you paste. A webhook URL is itself a credential.

## Suggesting a feature

Open a feature request in the repository concerned and describe the problem first: what you are monitoring, what you tried, and where it fell short. A problem statement gets a better answer than a finished design.

## Contributing code

1. For anything larger than a small fix, open an issue first so we can agree on the approach before you write it.
2. Fork the repository and branch from `main`.
3. Keep the change focused, add or update tests, and run the repository's own checks (each README says how).
4. Open a pull request that explains what changed and why, and links the issue.

By contributing you agree that your contribution is licensed under the license of the repository you contribute to (MPL-2.0 for the Terraform provider, MIT for lastping-app).

Everyone taking part is expected to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
