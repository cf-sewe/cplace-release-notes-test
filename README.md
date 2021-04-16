# cplace-release-notes-test

Repo for testing cplace release note generation.
This repo simulates an typical cplace integration repo and includes a `parent-repos.json` file which defines the child repositories to be included.

cplace release notes are generated using [cplace-cli](https://github.com/collaborationFactory/cplace-npm-tools/), so please make sure it is installed.

## Creating a release manually

Perform the following steps on an integration repo:

- Checkout integration repo: `git clone <REPO>`
- Checkout all child repos: `cplace-cli repos --clone`
- Freeze the repos: `cplace-cli repos --write --freeze`
...

## Creating a release via GitHub Action

The creation of a customer release via an integration repository is typically automated via an GitHub action.
When a GitHub release is created, a GitHub action will run and execute following steps:

- todo

## Tests

- no changelog entry with `changelog:`
- no duplicate changelog entries
- changelog entry components are properly capitalized
- changelog at the beginning of commit message can be properly parsed
- changelog with preceding lines can be properly parsed
- changelog with succeeding lines can be properly parsed
- changelog entry in code-block (\`changelog:...\`) can be properly parsed
- changelog entries of child repositories are present
- changelog entry can be added via `explicits_xx.db`
- changelog entry can be replaced via `explicits_xx.db`
